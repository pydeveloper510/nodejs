# nodejs

Error: spawn ENOENT
    at errnoException (child_process.js:1000:11)
    at Process.ChildProcess._handle.onexit (child_process.js:791:34)


(function() {
    var childProcess = require("child_process");
    var oldSpawn = childProcess.spawn;
    function mySpawn() {
        console.log('spawn called');
        console.log(arguments);
        var result = oldSpawn.apply(this, arguments);
        return result;
    }
    childProcess.spawn = mySpawn;
})();
