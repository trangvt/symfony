## 2/ Create your First Page in Symfony
https://symfony.com/doc/3.4/page_creation.html

# Checking out the Project Structure
src/
	Your PHP code lives here.
		99% of the time, you'll be working in src/ (PHP files) or app/ (everything else).
		As you keep reading, you'll learn what can be done inside each of these.

# Bundles & Configuration
+ Your Symfony application comes pre-installed (cài đặt sẵn) with a collection of bundles

+ Bundles are similar to the idea of a plugin, but with one important difference: all functionality in a Symfony application comes from a bundle.
	vendor/symfony/symfony/src/Symfony/Bundle/FrameworkBundle/FrameworkBundle.php
	vendor/symfony/symfony/src/Symfony/Bundle/TwigBundle/TwigBundle.php

+ Bundles are registered in your `app/AppKernel.php` file (a rare PHP file in the app/ directory) and each gives you more tools, sometimes called `services`:

```PHP
use Symfony\Component\HttpKernel\Kernel;
use Symfony\Component\Config\Loader\LoaderInterface;

class AppKernel extends Kernel
{
    public function registerBundles()
    {
        $bundles = [
            new Symfony\Bundle\FrameworkBundle\FrameworkBundle(),
            new Symfony\Bundle\TwigBundle\TwigBundle(),
            ...
        ];

        return $bundles;
    }
```

+ Eventually (Cuối cùng), you'll download and add more third-party bundles to your app in order to get even more tools. Imagine a bundle that helps you create paginated lists

+ You can control how your bundles behave via the `app/config/config.yml` file