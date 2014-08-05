input some version changes here~

* sails new project_name --linker in no longer work?

[SailsJS v0.10 create new project --linker not working Gruntfile.js not used](http://stackoverflow.com/questions/22042260/sailsjs-v0-10-create-new-project-linker-not-working-gruntfile-js-not-used)

目前0.10.1版本中：tasks/config/sync.js下：

```shell
module.exports = function(grunt) {

	grunt.config.set('sync', {
		dev: {
			files: [{
				cwd: './assets',
				src: ['**/*.!(coffee)'],
				dest: '.tmp/public'
			}]
		}
	});

	grunt.loadNpmTasks('grunt-sync');
};
```

都会编译到 .tmp/public下面
