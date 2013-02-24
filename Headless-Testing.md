# �w�b�h���X�e�X�g

PhantomJS�̎�ȃ��[�X�P�[�X��1�́AWeb�A�v���P�[�V������ **�w�b�h���X�e�X�g** �ł��B����̓v���R�~�b�g�t�b�N���A����ьp���I�ȓ����V�X�e���̈ꕔ�Ƃ��āA��ʓI�ȃR�}���h���C���x�[�X�̃e�X�g�ɓK���Ă��܂��B
<!-- One major use case of PhantomJS is **headless testing** of web applications. It is suitable for general command-line based testing, within a precommit hook, and as part of a continuous integration system. -->

## �e�X�g�t���[�����[�N
<!-- ## Test Frameworks -->

PhantomJS���̂̓e�X�g�t���[�����[�N�ł� **����܂���** �BPhantomJS�͓K�؂ȃe�X�g�����i�[����āA�e�X�g���N�����邽�߂����Ɏg�p����܂��B
<!-- PhantomJS itself is **not** a test framework, it is only used to launch the tests via a suitable test runner. -->

���̕\�́A���܂��܃e�X�g�t���[�����[�N�Ƃ���ɑΉ�����e�X�g�����i�[�̈ꗗ���܂Ƃ߂Ă��܂��B�t���[�����[�N������/�O���̃T�[�h�p�[�e�B�������i�[��K�v�Ƃ��Ȃ��ꍇ�A "built-in"�Ƃ��Ă��܂��B
<!-- The following table summarizes the list of various test frameworks and the corresponding test runners. If the framework does not need an external/third-party runner, it is marked as "built-in". -->

| Framework  | Test Runner |
|:-----------|:------------|
| [Buster.JS](http://busterjs.org)| built-in|
| [Capybara](http://jnicklas.github.com/capybara) |[Poltergeist](https://github.com/jonleighton/poltergeist), [Terminus](http://terminus.jcoglan.com)
| [Mocha](http://visionmedia.github.com/mocha) | [mocha-phantomjs](http://metaskills.net/mocha-phantomjs) |
| [FuncUnit](http://funcunit.com) | built-in|
| [Hiro](http://hirojs.com) | built-in|
| [Jasmine](https://github.com/pivotal/jasmine) | [Chutzpah](http://chutzpah.codeplex.com), [grunt-jasmine-runner](https://github.com/jasmine-contrib/grunt-jasmine-runner), [guard-jasmine](https://github.com/netzpirat/guard-jasmine), [phantom-jasmine](https://github.com/jcarver989/phantom-jasmine)|
| [JsTestDriver](http://code.google.com/p/js-test-driver/) | [js-test-driver-phantomjs](https://github.com/larrymyers/js-test-driver-phantomjs) |
| [Robot Framework](http://code.google.com/p/robotframework/) | [phantomrobot](https://github.com/datakurre/phantomrobot)|
| [QUnit](http://qunitjs.com) | [built-in](https://github.com/jquery/qunit/tree/master/addons/phantomjs), [Chutzpah](http://chutzpah.codeplex.com), [JS Test Runner](http://js-testrunner.codehaus.org), [QUnited](http://github.com/aaronroyer/qunited)|
| [Testacular](http://vojtajina.github.com/testacular) | built-in |
| [Testem](https://github.com/airportyh/testem) | built-in |
| [WebDriver](http://dvcs.w3.org/hg/webdriver/raw-file/tip/webdriver-spec.html) | [GhostDriver](https://github.com/detro/ghostdriver)|
| [wru](https://github.com/WebReflection/wru) | built-in|
| [YUITest](http://yuilibrary.com/projects/yuitest) | [Grover](https://github.com/davglass/grover), [phantomjs-yuitest](https://github.com/metafeather/phantomjs-yuitest) |

PhantomJS��`examples`�f�B���N�g���̒���[run-qunit](https://github.com/ariya/phantomjs/blob/master/examples/run-qunit.js)��[run-jasmine](https://github.com/ariya/phantomjs/blob/master/examples/run-jasmine.js)���܂�ł��܂��B�������A�����͎���̂��߂ł���A���ۂɎg�p�����ŕK�v�ȃ��|�[�g�@�\������܂���I
<!-- PhantomJS includes [run-qunit](https://github.com/ariya/phantomjs/blob/master/examples/run-qunit.js) and [run-jasmine](https://github.com/ariya/phantomjs/blob/master/examples/run-jasmine.js) in its `examples` subdirectory. However, these are for illustration purposes and lack important reporting features necessary for real-world uses! -->

## PhantomJS tailored testing

�܂��A�e�X�g��ړI�Ƃ����֗��ō����x���ȋ@�\��񋟂��邽�߂�PhantomJS�̏�ɍ\�z����Ă���[projects](./Related-Projects.md)������������܂�:
<!-- In addition, there are [[projects|Related Projects]] which are built on top of PhantomJS to provide convenient high-level functionality for testing purposes: -->

* [Casper.js](http://casperjs.org)�̓X�N���v�g�i�r�Q�[�V�����ƃe�X�g���\�z����̂ɗL�p�ł�
* [Lotte](https://github.com/StanAngeloff/lotte)��jQuery���C�N�ȃ��\�b�h��`�F�[���A���̑��ɃA�T�[�V�������W�b�N��ǉ����Ă��܂�
* [WebSpecter](https://github.com/jgonera/webspecter)��Web�A�v���P�[�V�����̂��߂�BDD�X�^�C���̎󂯓���e�X�g�̃t���[�����[�N�ł�

<!-- * [Casper.js](http://casperjs.org) is useful to build scripted navigation and testing -->
<!-- * [Lotte](https://github.com/StanAngeloff/lotte) adds jQuery-like methods, chaining, and more assertion logic -->
<!-- * [WebSpecter](https://github.com/jgonera/webspecter) is a BDD-style acceptance test framework for web applications -->

## �p���I�C���e�O���[�V�����V�X�e��
<!-- ## Continuous Integration Systems -->

**[Jenkins](http://jenkins-ci.org/)** �� **[TeamCity](http://www.jetbrains.com/teamcity/)** �Ƃ�����CI�V�X�e����PhantomJS���g�p����ꍇ�́A���ʂȃZ�b�g�A�b�v�͕K�v����܂���BPhantomJS���X���[�u/�r���h�G�[�W�F���g��Ő������C���X�g�[������Ă��āA���s�\�ł��邱�Ƃ��m�F���Ă��������B
<!-- Using PhantomJS with CI system such as **[Jenkins](http://jenkins-ci.org/)** or **[TeamCity](http://www.jetbrains.com/teamcity/)** does not require special setup. Make sure PhantomJS is installed properly on the slave/build agent and it is ready to go. -->

PhantomJS��Linux��Ńs���A�w�b�h���X�ł��邽�߁A�G�[�W�F���g�͔C�ӂ�GUI�̃C���X�g�[����Ŏ��s���邱�Ƃ��ł��܂��B���̕��@�́AX11�̂Ȃ��x�A�{�[����Linux�V�X�e���ł�PhantomJS�͖�肠��܂���B�����Amazon EC2��Heroku�̃C���X�^���X��Ōy�ʂȃr���h�G�[�W�F���g�𑽐��N�����邱�Ƃ��\�ɂȂ�܂��B
<!-- Since PhantomJS is purely headless on Linux, the agent can run on an installation with any GUI. This means, a barebone Linux system without X11 is not a problem for PhantomJS. It makes it possible to spawn light build agents on Amazon EC2 or Heroku instances. -->

�l�C�z�X�e�b�hCI�V�X�e���ł��� **[Travis CI](http://about.travis-ci.org/)** �́APhantomJS�ɑg�ݍ��݃T�|�[�g����Ă��܂��B�ڍׂ�[its documentation](http://about.travis-ci.org/docs/user/gui-and-headless-browsers/)���Q�Ƃ��Ă��������B
<!-- **[Travis CI](http://about.travis-ci.org/)**, a popular hosted CI system, has built-in support for PhantomJS. See [its documentation](http://about.travis-ci.org/docs/user/gui-and-headless-browsers/) for details. -->