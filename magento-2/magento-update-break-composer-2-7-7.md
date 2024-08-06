#Composer version 2.7.7 breaks Magento 2.4.7-p1 update

```bash
composer require-commerce magento/product-community-edition 2.4.7-p1 --no-update
```


```php
Fatal error: Declaration of Magento\ComposerRootUpdatePlugin\Plugin\Commands\OverrideRequireCommand::execute(Symfony\Component\Console\Input\InputInterface $input, Symfony\Component\Console\Output\OutputInterface $output) must be compatible with Composer\Command\RequireCommand::execute(Symfony\Component\Console\Input\InputInterface $input, Symfony\Component\Console\Output\OutputInterface $output): int in /Users/martin/PhpstormProjects/hocras/project/vendor/magento/composer-root-update-plugin/Plugin/Commands/OverrideRequireCommand.php on line 173
```

Quick fix is to downgrade composer to version 2.6.6

```bash
composer self-update 2.6.6
```
