- [ ] Add tabs
- [ ] Add slider
- [ ] Add horizontal and vertical navigation
- [ ] On `_typography.scss` line 35 change to `$base-line-height;`
- [ ] Fix buttons styles
- [ ] Change all max for min
- [ ] Fix Gruntfile.js rsync task to this:
```
rsync: {
	options: {
		args: ["--verbose"],
		exclude: ["sass", "*~", "*.swp", ".*", "*.md", "node_modules", "prod", "bower_components", "Gruntfile.js", "package.json", "bower.json"],
		recursive: true
	},
	dist: {
		options: {
			src: "<%= config.dev %>",
			dest: "<%= config.prod %>"
		}
	}
}
```
- [ ] fix imagemin to this:
```
imagemin: {
	target: {
		options: {
			optimizationLevel: 7
		},
		files: [{
			expand: true,
			cwd: '<%= config.dev %>/img',
			src: '*.{png,jpg,jpeg}',
			dest: '<%= config.prod %>/img'
		}]
	}
}
```
