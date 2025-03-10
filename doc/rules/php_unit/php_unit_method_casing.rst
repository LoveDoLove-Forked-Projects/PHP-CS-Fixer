===============================
Rule ``php_unit_method_casing``
===============================

Enforce camel (or snake) case for PHPUnit test methods, following configuration.

Configuration
-------------

``case``
~~~~~~~~

Apply camel or snake case to test methods.

Allowed values: ``'camel_case'`` and ``'snake_case'``

Default value: ``'camel_case'``

Examples
--------

Example #1
~~~~~~~~~~

*Default* configuration.

.. code-block:: diff

   --- Original
   +++ New
    <?php
    class MyTest extends \PhpUnit\FrameWork\TestCase
    {
   -    public function test_my_code() {}
   +    public function testMyCode() {}
    }

Example #2
~~~~~~~~~~

With configuration: ``['case' => 'snake_case']``.

.. code-block:: diff

   --- Original
   +++ New
    <?php
    class MyTest extends \PhpUnit\FrameWork\TestCase
    {
   -    public function testMyCode() {}
   +    public function test_my_code() {}
    }

Example #3
~~~~~~~~~~

*Default* configuration.

.. code-block:: diff

   --- Original
   +++ New
    <?php
    use \PHPUnit\Framework\Attributes\Test;
    class MyTest extends \PhpUnit\FrameWork\TestCase
    {
        #[PHPUnit\Framework\Attributes\Test]
   -    public function test_my_code() {}
   +    public function testMyCode() {}
    }

Example #4
~~~~~~~~~~

With configuration: ``['case' => 'snake_case']``.

.. code-block:: diff

   --- Original
   +++ New
    <?php
    use \PHPUnit\Framework\Attributes\Test;
    class MyTest extends \PhpUnit\FrameWork\TestCase
    {
        #[PHPUnit\Framework\Attributes\Test]
   -    public function testMyCode() {}
   +    public function test_my_code() {}
    }

Rule sets
---------

The rule is part of the following rule sets:

- `@PhpCsFixer <./../../ruleSets/PhpCsFixer.rst>`_
- `@Symfony <./../../ruleSets/Symfony.rst>`_

References
----------

- Fixer class: `PhpCsFixer\\Fixer\\PhpUnit\\PhpUnitMethodCasingFixer <./../../../src/Fixer/PhpUnit/PhpUnitMethodCasingFixer.php>`_
- Test class: `PhpCsFixer\\Tests\\Fixer\\PhpUnit\\PhpUnitMethodCasingFixerTest <./../../../tests/Fixer/PhpUnit/PhpUnitMethodCasingFixerTest.php>`_

The test class defines officially supported behaviour. Each test case is a part of our backward compatibility promise.
