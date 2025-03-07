:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the Callable.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_Callable:

Callable
========

An object representing a method in a certain object that can be called.

Description
-----------

``Callable`` is a first class object which can be held in variables and passed to functions. It represents a given method in an :ref:`Object<class_Object>`, and is typically used for signal callbacks.

\ **Example:**\ 


.. tabs::

 .. code-tab:: gdscript

    func print_args(arg1, arg2, arg3 = ""):
        prints(arg1, arg2, arg3)
    
    func test():
        var callable = Callable(self, "print_args")
        callable.call("hello", "world")  # Prints "hello world ".
        callable.call(Vector2.UP, 42, callable)  # Prints "(0, -1) 42 Node(Node.gd)::print_args".
        callable.call("invalid")  # Invalid call, should have at least 2 arguments.

 .. code-tab:: csharp

    public void PrintArgs(object arg1, object arg2, object arg3 = null)
    {
        GD.PrintS(arg1, arg2, arg3);
    }
    
    public void Test()
    {
        Callable callable = new Callable(this, nameof(PrintArgs));
        callable.Call("hello", "world"); // Prints "hello world null".
        callable.Call(Vector2.Up, 42, callable); // Prints "(0, -1) 42 Node(Node.cs)::PrintArgs".
        callable.Call("invalid"); // Invalid call, should have at least 2 arguments.
    }



Constructors
------------

+---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Callable<class_Callable>` | :ref:`Callable<class_Callable_constructor_Callable>` **(** **)**                                                                                |
+---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Callable<class_Callable>` | :ref:`Callable<class_Callable_constructor_Callable>` **(** :ref:`Callable<class_Callable>` from **)**                                           |
+---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Callable<class_Callable>` | :ref:`Callable<class_Callable_constructor_Callable>` **(** :ref:`Object<class_Object>` object, :ref:`StringName<class_StringName>` method **)** |
+---------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+

Methods
-------

+-------------------------------------+-------------------------------------------------------------------------------------------------------------+
| :ref:`Callable<class_Callable>`     | :ref:`bind<class_Callable_method_bind>` **(** ... **)** |vararg| |const|                                    |
+-------------------------------------+-------------------------------------------------------------------------------------------------------------+
| :ref:`Variant<class_Variant>`       | :ref:`call<class_Callable_method_call>` **(** ... **)** |vararg| |const|                                    |
+-------------------------------------+-------------------------------------------------------------------------------------------------------------+
| void                                | :ref:`call_deferred<class_Callable_method_call_deferred>` **(** ... **)** |vararg| |const|                  |
+-------------------------------------+-------------------------------------------------------------------------------------------------------------+
| :ref:`StringName<class_StringName>` | :ref:`get_method<class_Callable_method_get_method>` **(** **)** |const|                                     |
+-------------------------------------+-------------------------------------------------------------------------------------------------------------+
| :ref:`Object<class_Object>`         | :ref:`get_object<class_Callable_method_get_object>` **(** **)** |const|                                     |
+-------------------------------------+-------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`               | :ref:`get_object_id<class_Callable_method_get_object_id>` **(** **)** |const|                               |
+-------------------------------------+-------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`               | :ref:`hash<class_Callable_method_hash>` **(** **)** |const|                                                 |
+-------------------------------------+-------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`             | :ref:`is_custom<class_Callable_method_is_custom>` **(** **)** |const|                                       |
+-------------------------------------+-------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`             | :ref:`is_null<class_Callable_method_is_null>` **(** **)** |const|                                           |
+-------------------------------------+-------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`             | :ref:`is_standard<class_Callable_method_is_standard>` **(** **)** |const|                                   |
+-------------------------------------+-------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`             | :ref:`is_valid<class_Callable_method_is_valid>` **(** **)** |const|                                         |
+-------------------------------------+-------------------------------------------------------------------------------------------------------------+
| void                                | :ref:`rpc<class_Callable_method_rpc>` **(** ... **)** |vararg| |const|                                      |
+-------------------------------------+-------------------------------------------------------------------------------------------------------------+
| void                                | :ref:`rpc_id<class_Callable_method_rpc_id>` **(** :ref:`int<class_int>` peer_id, ... **)** |vararg| |const| |
+-------------------------------------+-------------------------------------------------------------------------------------------------------------+
| :ref:`Callable<class_Callable>`     | :ref:`unbind<class_Callable_method_unbind>` **(** :ref:`int<class_int>` argcount **)** |const|              |
+-------------------------------------+-------------------------------------------------------------------------------------------------------------+

Operators
---------

+-------------------------+--------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>` | :ref:`operator !=<class_Callable_operator_neq_bool>` **(** :ref:`Callable<class_Callable>` right **)** |
+-------------------------+--------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>` | :ref:`operator ==<class_Callable_operator_eq_bool>` **(** :ref:`Callable<class_Callable>` right **)**  |
+-------------------------+--------------------------------------------------------------------------------------------------------+

Constructor Descriptions
------------------------

.. _class_Callable_constructor_Callable:

- :ref:`Callable<class_Callable>` **Callable** **(** **)**

Constructs a null ``Callable`` with no object nor method bound.

----

- :ref:`Callable<class_Callable>` **Callable** **(** :ref:`Callable<class_Callable>` from **)**

Constructs a ``Callable`` as a copy of the given ``Callable``.

----

- :ref:`Callable<class_Callable>` **Callable** **(** :ref:`Object<class_Object>` object, :ref:`StringName<class_StringName>` method **)**

Creates a new ``Callable`` for the method called ``method`` in the specified ``object``.

Method Descriptions
-------------------

.. _class_Callable_method_bind:

- :ref:`Callable<class_Callable>` **bind** **(** ... **)** |vararg| |const|

Returns a copy of this ``Callable`` with the arguments bound. Bound arguments are passed after the arguments supplied by :ref:`call<class_Callable_method_call>`.

----

.. _class_Callable_method_call:

- :ref:`Variant<class_Variant>` **call** **(** ... **)** |vararg| |const|

Calls the method represented by this ``Callable``. Arguments can be passed and should match the method's signature.

----

.. _class_Callable_method_call_deferred:

- void **call_deferred** **(** ... **)** |vararg| |const|

Calls the method represented by this ``Callable`` in deferred mode, i.e. during the idle frame. Arguments can be passed and should match the method's signature.

----

.. _class_Callable_method_get_method:

- :ref:`StringName<class_StringName>` **get_method** **(** **)** |const|

Returns the name of the method represented by this ``Callable``.

----

.. _class_Callable_method_get_object:

- :ref:`Object<class_Object>` **get_object** **(** **)** |const|

Returns the object on which this ``Callable`` is called.

----

.. _class_Callable_method_get_object_id:

- :ref:`int<class_int>` **get_object_id** **(** **)** |const|

Returns the ID of this ``Callable``'s object (see :ref:`Object.get_instance_id<class_Object_method_get_instance_id>`).

----

.. _class_Callable_method_hash:

- :ref:`int<class_int>` **hash** **(** **)** |const|

Returns the 32-bit hash value of this ``Callable``'s object.

\ **Note:** ``Callable``\ s with equal content will always produce identical hash values. However, the reverse is not true. Returning identical hash values does *not* imply the callables are equal, because different callables can have identical hash values due to hash collisions. The engine uses a 32-bit hash algorithm for :ref:`hash<class_Callable_method_hash>`.

----

.. _class_Callable_method_is_custom:

- :ref:`bool<class_bool>` **is_custom** **(** **)** |const|

Returns ``true`` if this ``Callable`` is a custom callable whose behavior differs based on implementation details. Custom callables are used in the engine for various reasons. If ``true``, you can't use :ref:`get_method<class_Callable_method_get_method>`.

----

.. _class_Callable_method_is_null:

- :ref:`bool<class_bool>` **is_null** **(** **)** |const|

Returns ``true`` if this ``Callable`` has no target to call the method on.

----

.. _class_Callable_method_is_standard:

- :ref:`bool<class_bool>` **is_standard** **(** **)** |const|

Returns ``true`` if this ``Callable`` is a standard callable, referencing an object and a method using a :ref:`StringName<class_StringName>`.

----

.. _class_Callable_method_is_valid:

- :ref:`bool<class_bool>` **is_valid** **(** **)** |const|

Returns ``true`` if the object exists and has a valid function assigned, or is a custom callable.

----

.. _class_Callable_method_rpc:

- void **rpc** **(** ... **)** |vararg| |const|

Perform an RPC (Remote Procedure Call). This is used for multiplayer and is normally not available unless the function being called has been marked as *RPC*. Calling it on unsupported functions will result in an error.

----

.. _class_Callable_method_rpc_id:

- void **rpc_id** **(** :ref:`int<class_int>` peer_id, ... **)** |vararg| |const|

Perform an RPC (Remote Procedure Call) on a specific peer ID (see multiplayer documentation for reference). This is used for multiplayer and is normally not available unless the function being called has been marked as *RPC*. Calling it on unsupported functions will result in an error.

----

.. _class_Callable_method_unbind:

- :ref:`Callable<class_Callable>` **unbind** **(** :ref:`int<class_int>` argcount **)** |const|

Returns a copy of this ``Callable`` with the arguments unbound. Calling the returned ``Callable`` will call the method without the extra arguments that are supplied in the ``Callable`` on which you are calling this method.

Operator Descriptions
---------------------

.. _class_Callable_operator_neq_bool:

- :ref:`bool<class_bool>` **operator !=** **(** :ref:`Callable<class_Callable>` right **)**

Returns ``true`` if both ``Callable``\ s invoke different targets.

----

.. _class_Callable_operator_eq_bool:

- :ref:`bool<class_bool>` **operator ==** **(** :ref:`Callable<class_Callable>` right **)**

Returns ``true`` if both ``Callable``\ s invoke the same custom target.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
