How to install
==============

  1. cd src/
  2. git clone git://github.com/mitchpolska/RouterBundle.git
  3. Open file: vendor/symfony/src/Symfony/Bundle/FrameworkBundle/Resources/config/routing.xml
  4. Find and replace parameters:
     
        <parameter key="router.options.generator_base_class">ITZ\RouterBundle\Component\Routing\Generator\UrlGenerator</parameter>
        <parameter key="router.options.matcher_dumper_class">ITZ\RouterBundle\Component\Routing\Matcher\Dumper\PhpMatcherDumper</parameter>
  
  5. Clear cache

Quick example
=============

	_some_route:
		pattern:   /something/{slug}
		defaults: { _controller: AcmeUserBundle:Something:something }
		requirements:
		  _host: http://{somesubdomain}.host.dev
		  somesubdomain: /^option1|option2$/
		  _scheme: http
