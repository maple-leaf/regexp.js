require('shelljs/global');

var fs = require('fs');

var parse = require('./lib/parser.js').parse;

var parseTests = JSON.parse(fs.readFileSync('test/parse_input.json') || '[]');
var parseResult = JSON.parse(fs.readFileSync('test/parse_output.json') || '[]');

desc("Run tests.");
task("test", function() {
    exec('node ./test.js')
});

desc("Create refrence file.");
task("ref", function() {
    var arr = parseTests.map(parse);

    fs.writeFileSync('test/parse_output.json', JSON.stringify(arr, null, 2));
});
