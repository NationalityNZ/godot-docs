:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the GDScript.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_GDScript:

GDScript
========

**Inherits:** :ref:`Script<class_Script>` **<** :ref:`Resource<class_Resource>` **<** :ref:`RefCounted<class_RefCounted>` **<** :ref:`Object<class_Object>`

A script implemented in the GDScript programming language.

Description
-----------

A script implemented in the GDScript programming language. The script extends the functionality of all objects that instance it.

\ :ref:`new<class_GDScript_method_new>` creates a new instance of the script. :ref:`Object.set_script<class_Object_method_set_script>` extends an existing object, if that object's class matches one of the script's base classes.

Tutorials
---------

- :doc:`GDScript documentation index <../tutorials/scripting/gdscript/index>`

Methods
-------

+-----------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`PackedByteArray<class_PackedByteArray>` | :ref:`get_as_byte_code<class_GDScript_method_get_as_byte_code>` **(** **)** |const| |
+-----------------------------------------------+-------------------------------------------------------------------------------------+
| :ref:`Variant<class_Variant>`                 | :ref:`new<class_GDScript_method_new>` **(** ... **)** |vararg|                      |
+-----------------------------------------------+-------------------------------------------------------------------------------------+

Method Descriptions
-------------------

.. _class_GDScript_method_get_as_byte_code:

- :ref:`PackedByteArray<class_PackedByteArray>` **get_as_byte_code** **(** **)** |const|

Returns byte code for the script source code.

----

.. _class_GDScript_method_new:

- :ref:`Variant<class_Variant>` **new** **(** ... **)** |vararg|

Returns a new instance of the script.

For example:

::

    var MyClass = load("myclass.gd")
    var instance = MyClass.new()
    assert(instance.get_script() == MyClass)

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
