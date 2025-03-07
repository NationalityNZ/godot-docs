:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the ScrollBar.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_ScrollBar:

ScrollBar
=========

**Inherits:** :ref:`Range<class_Range>` **<** :ref:`Control<class_Control>` **<** :ref:`CanvasItem<class_CanvasItem>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

**Inherited By:** :ref:`HScrollBar<class_HScrollBar>`, :ref:`VScrollBar<class_VScrollBar>`

Base class for scroll bars.

Description
-----------

Scrollbars are a :ref:`Range<class_Range>`-based :ref:`Control<class_Control>`, that display a draggable area (the size of the page). Horizontal (:ref:`HScrollBar<class_HScrollBar>`) and Vertical (:ref:`VScrollBar<class_VScrollBar>`) versions are available.

Properties
----------

+---------------------------+----------------------------------------------------------+----------+
| :ref:`float<class_float>` | :ref:`custom_step<class_ScrollBar_property_custom_step>` | ``-1.0`` |
+---------------------------+----------------------------------------------------------+----------+

Signals
-------

.. _class_ScrollBar_signal_scrolling:

- **scrolling** **(** **)**

Emitted when the scrollbar is being scrolled.

Property Descriptions
---------------------

.. _class_ScrollBar_property_custom_step:

- :ref:`float<class_float>` **custom_step**

+-----------+------------------------+
| *Default* | ``-1.0``               |
+-----------+------------------------+
| *Setter*  | set_custom_step(value) |
+-----------+------------------------+
| *Getter*  | get_custom_step()      |
+-----------+------------------------+

Overrides the step used when clicking increment and decrement buttons or when using arrow keys when the ``ScrollBar`` is focused.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
