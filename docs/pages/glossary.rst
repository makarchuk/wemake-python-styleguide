.. _glossary:

Glossary
========

First of all, we should speak the same language.
Here we collect all the specific terms that are used in this project.

.. glossary::

   plugin
      A plugin for ``flake8``, developed following `official guides <flake8.pycqa.org/en/latest/plugin-development/index.html>`_.

   wemake_python_styleguide
      ``flake8`` plugin.

      Set of rules of how we write ``python`` code in `wemake.services <https://wemake.services>`_.

   checker
      ``flake8`` plugin compatible class that is used as an entry point.
      Entry point and violation codes are defined in ``pyproject.toml``.
      This class runs all visitors that exist in our style guide.

  transformation
      A way we change existing nodes. We can add properties, fix errors,
      delete or replace some nodes.

      The reasons for these actions are: developer experience, simplicity,
      consistency across different versions, bug-fixing.

   visitor
      An object that goes through set of ``ast``, ``tokenize``, or other
      nodes to find violation of our rules.

   violation
      Stylistic or semantic error.

      We count each violation definition
      as a strict rule: how should we behave in different situations.

      Each violation has its own reasoning, solution, and code examples.
      Some violations can be configured,
      some violations contains related constants.
