:github_url: hide

.. DO NOT EDIT THIS FILE!!!
.. Generated automatically from Godot engine sources.
.. Generator: https://github.com/godotengine/godot/tree/master/doc/tools/make_rst.py.
.. XML source: https://github.com/godotengine/godot/tree/master/doc/classes/VideoStreamPlayer.xml.

.. _class_VideoStreamPlayer:

VideoStreamPlayer
=================

**Inherits:** :ref:`Control<class_Control>` **<** :ref:`CanvasItem<class_CanvasItem>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

Control for playing video streams.

Description
-----------

Control node for playing video streams using :ref:`VideoStream<class_VideoStream>` resources.

Supported video formats are `Ogg Theora <https://www.theora.org/>`__ (``.ogv``, :ref:`VideoStreamTheora<class_VideoStreamTheora>`) and any format exposed via a GDExtension plugin.

\ **Note:** Due to a bug, VideoStreamPlayer does not support localization remapping yet.

\ **Warning:** On Web, video playback *will* perform poorly due to missing architecture-specific assembly optimizations.

Properties
----------

+---------------------------------------+--------------------------------------------------------------------------+---------------+
| :ref:`int<class_int>`                 | :ref:`audio_track<class_VideoStreamPlayer_property_audio_track>`         | ``0``         |
+---------------------------------------+--------------------------------------------------------------------------+---------------+
| :ref:`bool<class_bool>`               | :ref:`autoplay<class_VideoStreamPlayer_property_autoplay>`               | ``false``     |
+---------------------------------------+--------------------------------------------------------------------------+---------------+
| :ref:`int<class_int>`                 | :ref:`buffering_msec<class_VideoStreamPlayer_property_buffering_msec>`   | ``500``       |
+---------------------------------------+--------------------------------------------------------------------------+---------------+
| :ref:`StringName<class_StringName>`   | :ref:`bus<class_VideoStreamPlayer_property_bus>`                         | ``&"Master"`` |
+---------------------------------------+--------------------------------------------------------------------------+---------------+
| :ref:`bool<class_bool>`               | :ref:`expand<class_VideoStreamPlayer_property_expand>`                   | ``false``     |
+---------------------------------------+--------------------------------------------------------------------------+---------------+
| :ref:`bool<class_bool>`               | :ref:`paused<class_VideoStreamPlayer_property_paused>`                   | ``false``     |
+---------------------------------------+--------------------------------------------------------------------------+---------------+
| :ref:`VideoStream<class_VideoStream>` | :ref:`stream<class_VideoStreamPlayer_property_stream>`                   |               |
+---------------------------------------+--------------------------------------------------------------------------+---------------+
| :ref:`float<class_float>`             | :ref:`stream_position<class_VideoStreamPlayer_property_stream_position>` |               |
+---------------------------------------+--------------------------------------------------------------------------+---------------+
| :ref:`float<class_float>`             | :ref:`volume<class_VideoStreamPlayer_property_volume>`                   |               |
+---------------------------------------+--------------------------------------------------------------------------+---------------+
| :ref:`float<class_float>`             | :ref:`volume_db<class_VideoStreamPlayer_property_volume_db>`             | ``0.0``       |
+---------------------------------------+--------------------------------------------------------------------------+---------------+

Methods
-------

+-----------------------------------+------------------------------------------------------------------------------------------------+
| :ref:`String<class_String>`       | :ref:`get_stream_name<class_VideoStreamPlayer_method_get_stream_name>` **(** **)** |const|     |
+-----------------------------------+------------------------------------------------------------------------------------------------+
| :ref:`Texture2D<class_Texture2D>` | :ref:`get_video_texture<class_VideoStreamPlayer_method_get_video_texture>` **(** **)** |const| |
+-----------------------------------+------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`           | :ref:`is_playing<class_VideoStreamPlayer_method_is_playing>` **(** **)** |const|               |
+-----------------------------------+------------------------------------------------------------------------------------------------+
| void                              | :ref:`play<class_VideoStreamPlayer_method_play>` **(** **)**                                   |
+-----------------------------------+------------------------------------------------------------------------------------------------+
| void                              | :ref:`stop<class_VideoStreamPlayer_method_stop>` **(** **)**                                   |
+-----------------------------------+------------------------------------------------------------------------------------------------+

Signals
-------

.. _class_VideoStreamPlayer_signal_finished:

- **finished** **(** **)**

Emitted when playback is finished.

Property Descriptions
---------------------

.. _class_VideoStreamPlayer_property_audio_track:

- :ref:`int<class_int>` **audio_track**

+-----------+------------------------+
| *Default* | ``0``                  |
+-----------+------------------------+
| *Setter*  | set_audio_track(value) |
+-----------+------------------------+
| *Getter*  | get_audio_track()      |
+-----------+------------------------+

The embedded audio track to play.

----

.. _class_VideoStreamPlayer_property_autoplay:

- :ref:`bool<class_bool>` **autoplay**

+-----------+---------------------+
| *Default* | ``false``           |
+-----------+---------------------+
| *Setter*  | set_autoplay(value) |
+-----------+---------------------+
| *Getter*  | has_autoplay()      |
+-----------+---------------------+

If ``true``, playback starts when the scene loads.

----

.. _class_VideoStreamPlayer_property_buffering_msec:

- :ref:`int<class_int>` **buffering_msec**

+-----------+---------------------------+
| *Default* | ``500``                   |
+-----------+---------------------------+
| *Setter*  | set_buffering_msec(value) |
+-----------+---------------------------+
| *Getter*  | get_buffering_msec()      |
+-----------+---------------------------+

Amount of time in milliseconds to store in buffer while playing.

----

.. _class_VideoStreamPlayer_property_bus:

- :ref:`StringName<class_StringName>` **bus**

+-----------+----------------+
| *Default* | ``&"Master"``  |
+-----------+----------------+
| *Setter*  | set_bus(value) |
+-----------+----------------+
| *Getter*  | get_bus()      |
+-----------+----------------+

Audio bus to use for sound playback.

----

.. _class_VideoStreamPlayer_property_expand:

- :ref:`bool<class_bool>` **expand**

+-----------+-------------------+
| *Default* | ``false``         |
+-----------+-------------------+
| *Setter*  | set_expand(value) |
+-----------+-------------------+
| *Getter*  | has_expand()      |
+-----------+-------------------+

If ``true``, the video scales to the control size. Otherwise, the control minimum size will be automatically adjusted to match the video stream's dimensions.

----

.. _class_VideoStreamPlayer_property_paused:

- :ref:`bool<class_bool>` **paused**

+-----------+-------------------+
| *Default* | ``false``         |
+-----------+-------------------+
| *Setter*  | set_paused(value) |
+-----------+-------------------+
| *Getter*  | is_paused()       |
+-----------+-------------------+

If ``true``, the video is paused.

----

.. _class_VideoStreamPlayer_property_stream:

- :ref:`VideoStream<class_VideoStream>` **stream**

+----------+-------------------+
| *Setter* | set_stream(value) |
+----------+-------------------+
| *Getter* | get_stream()      |
+----------+-------------------+

The assigned video stream. See description for supported formats.

----

.. _class_VideoStreamPlayer_property_stream_position:

- :ref:`float<class_float>` **stream_position**

+----------+----------------------------+
| *Setter* | set_stream_position(value) |
+----------+----------------------------+
| *Getter* | get_stream_position()      |
+----------+----------------------------+

The current position of the stream, in seconds.

\ **Note:** Changing this value won't have any effect as seeking is not implemented yet, except in video formats implemented by a GDExtension add-on.

----

.. _class_VideoStreamPlayer_property_volume:

- :ref:`float<class_float>` **volume**

+----------+-------------------+
| *Setter* | set_volume(value) |
+----------+-------------------+
| *Getter* | get_volume()      |
+----------+-------------------+

Audio volume as a linear value.

----

.. _class_VideoStreamPlayer_property_volume_db:

- :ref:`float<class_float>` **volume_db**

+-----------+----------------------+
| *Default* | ``0.0``              |
+-----------+----------------------+
| *Setter*  | set_volume_db(value) |
+-----------+----------------------+
| *Getter*  | get_volume_db()      |
+-----------+----------------------+

Audio volume in dB.

Method Descriptions
-------------------

.. _class_VideoStreamPlayer_method_get_stream_name:

- :ref:`String<class_String>` **get_stream_name** **(** **)** |const|

Returns the video stream's name, or ``"<No Stream>"`` if no video stream is assigned.

----

.. _class_VideoStreamPlayer_method_get_video_texture:

- :ref:`Texture2D<class_Texture2D>` **get_video_texture** **(** **)** |const|

Returns the current frame as a :ref:`Texture2D<class_Texture2D>`.

----

.. _class_VideoStreamPlayer_method_is_playing:

- :ref:`bool<class_bool>` **is_playing** **(** **)** |const|

Returns ``true`` if the video is playing.

\ **Note:** The video is still considered playing if paused during playback.

----

.. _class_VideoStreamPlayer_method_play:

- void **play** **(** **)**

Starts the video playback from the beginning. If the video is paused, this will not unpause the video.

----

.. _class_VideoStreamPlayer_method_stop:

- void **stop** **(** **)**

Stops the video playback and sets the stream position to 0.

\ **Note:** Although the stream position will be set to 0, the first frame of the video stream won't become the current frame.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
