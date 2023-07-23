# Comparing `tmp/mutwo.midi-0.8.1.tar.gz` & `tmp/mutwo.midi-0.9.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mutwo.midi-0.8.1.tar", last modified: Sun Aug 14 12:44:16 2022, max compression
+gzip compressed data, was "mutwo.midi-0.9.0.tar", last modified: Sun Oct 30 22:41:45 2022, max compression
```

## Comparing `mutwo.midi-0.8.1.tar` & `mutwo.midi-0.9.0.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2022-08-14 12:44:16.524181 mutwo.midi-0.8.1/
--rw-r--r--   0 circleci  (3434) circleci  (3434)    35149 2022-08-14 12:44:07.000000 mutwo.midi-0.8.1/LICENSE
--rw-r--r--   0 circleci  (3434) circleci  (3434)     1345 2022-08-14 12:44:16.520181 mutwo.midi-0.8.1/PKG-INFO
--rw-r--r--   0 circleci  (3434) circleci  (3434)      913 2022-08-14 12:44:07.000000 mutwo.midi-0.8.1/README.md
-drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2022-08-14 12:44:16.520181 mutwo.midi-0.8.1/mutwo/
-drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2022-08-14 12:44:16.520181 mutwo.midi-0.8.1/mutwo/midi_converters/
--rw-r--r--   0 circleci  (3434) circleci  (3434)      199 2022-08-14 12:44:07.000000 mutwo.midi-0.8.1/mutwo/midi_converters/__init__.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)    20768 2022-08-14 12:44:07.000000 mutwo.midi-0.8.1/mutwo/midi_converters/backends.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)     1266 2022-08-14 12:44:07.000000 mutwo.midi-0.8.1/mutwo/midi_converters/configurations.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)      753 2022-08-14 12:44:07.000000 mutwo.midi-0.8.1/mutwo/midi_converters/constants.py
--rw-r--r--   0 circleci  (3434) circleci  (3434)    40650 2022-08-14 12:44:07.000000 mutwo.midi-0.8.1/mutwo/midi_converters/frontends.py
-drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2022-08-14 12:44:16.520181 mutwo.midi-0.8.1/mutwo/midi_version/
--rw-r--r--   0 circleci  (3434) circleci  (3434)      142 2022-08-14 12:44:07.000000 mutwo.midi-0.8.1/mutwo/midi_version/__init__.py
-drwxr-xr-x   0 circleci  (3434) circleci  (3434)        0 2022-08-14 12:44:16.520181 mutwo.midi-0.8.1/mutwo.midi.egg-info/
--rw-r--r--   0 circleci  (3434) circleci  (3434)     1345 2022-08-14 12:44:16.000000 mutwo.midi-0.8.1/mutwo.midi.egg-info/PKG-INFO
--rw-r--r--   0 circleci  (3434) circleci  (3434)      419 2022-08-14 12:44:16.000000 mutwo.midi-0.8.1/mutwo.midi.egg-info/SOURCES.txt
--rw-r--r--   0 circleci  (3434) circleci  (3434)        1 2022-08-14 12:44:16.000000 mutwo.midi-0.8.1/mutwo.midi.egg-info/dependency_links.txt
--rw-r--r--   0 circleci  (3434) circleci  (3434)      112 2022-08-14 12:44:16.000000 mutwo.midi-0.8.1/mutwo.midi.egg-info/requires.txt
--rw-r--r--   0 circleci  (3434) circleci  (3434)        6 2022-08-14 12:44:16.000000 mutwo.midi-0.8.1/mutwo.midi.egg-info/top_level.txt
--rw-r--r--   0 circleci  (3434) circleci  (3434)      104 2022-08-14 12:44:07.000000 mutwo.midi-0.8.1/pyproject.toml
--rw-r--r--   0 circleci  (3434) circleci  (3434)       38 2022-08-14 12:44:16.524181 mutwo.midi-0.8.1/setup.cfg
--rw-r--r--   0 circleci  (3434) circleci  (3434)     1162 2022-08-14 12:44:07.000000 mutwo.midi-0.8.1/setup.py
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2022-10-30 22:41:45.835309 mutwo.midi-0.9.0/
+-rw-r--r--   0 circleci  (1001) circleci  (1002)    35149 2022-10-30 22:41:36.000000 mutwo.midi-0.9.0/LICENSE
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     1345 2022-10-30 22:41:45.835309 mutwo.midi-0.9.0/PKG-INFO
+-rw-r--r--   0 circleci  (1001) circleci  (1002)      913 2022-10-30 22:41:36.000000 mutwo.midi-0.9.0/README.md
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2022-10-30 22:41:45.831309 mutwo.midi-0.9.0/mutwo/
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2022-10-30 22:41:45.835309 mutwo.midi-0.9.0/mutwo/midi_converters/
+-rw-r--r--   0 circleci  (1001) circleci  (1002)      199 2022-10-30 22:41:36.000000 mutwo.midi-0.9.0/mutwo/midi_converters/__init__.py
+-rw-r--r--   0 circleci  (1001) circleci  (1002)    20768 2022-10-30 22:41:36.000000 mutwo.midi-0.9.0/mutwo/midi_converters/backends.py
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     1412 2022-10-30 22:41:36.000000 mutwo.midi-0.9.0/mutwo/midi_converters/configurations.py
+-rw-r--r--   0 circleci  (1001) circleci  (1002)      753 2022-10-30 22:41:36.000000 mutwo.midi-0.9.0/mutwo/midi_converters/constants.py
+-rw-r--r--   0 circleci  (1001) circleci  (1002)    41092 2022-10-30 22:41:36.000000 mutwo.midi-0.9.0/mutwo/midi_converters/frontends.py
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2022-10-30 22:41:45.835309 mutwo.midi-0.9.0/mutwo/midi_version/
+-rw-r--r--   0 circleci  (1001) circleci  (1002)      142 2022-10-30 22:41:36.000000 mutwo.midi-0.9.0/mutwo/midi_version/__init__.py
+drwxr-xr-x   0 circleci  (1001) circleci  (1002)        0 2022-10-30 22:41:45.831309 mutwo.midi-0.9.0/mutwo.midi.egg-info/
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     1345 2022-10-30 22:41:45.000000 mutwo.midi-0.9.0/mutwo.midi.egg-info/PKG-INFO
+-rw-r--r--   0 circleci  (1001) circleci  (1002)      419 2022-10-30 22:41:45.000000 mutwo.midi-0.9.0/mutwo.midi.egg-info/SOURCES.txt
+-rw-r--r--   0 circleci  (1001) circleci  (1002)        1 2022-10-30 22:41:45.000000 mutwo.midi-0.9.0/mutwo.midi.egg-info/dependency_links.txt
+-rw-r--r--   0 circleci  (1001) circleci  (1002)      112 2022-10-30 22:41:45.000000 mutwo.midi-0.9.0/mutwo.midi.egg-info/requires.txt
+-rw-r--r--   0 circleci  (1001) circleci  (1002)        6 2022-10-30 22:41:45.000000 mutwo.midi-0.9.0/mutwo.midi.egg-info/top_level.txt
+-rw-r--r--   0 circleci  (1001) circleci  (1002)      104 2022-10-30 22:41:36.000000 mutwo.midi-0.9.0/pyproject.toml
+-rw-r--r--   0 circleci  (1001) circleci  (1002)       38 2022-10-30 22:41:45.835309 mutwo.midi-0.9.0/setup.cfg
+-rw-r--r--   0 circleci  (1001) circleci  (1002)     1162 2022-10-30 22:41:36.000000 mutwo.midi-0.9.0/setup.py
```

### Comparing `mutwo.midi-0.8.1/LICENSE` & `mutwo.midi-0.9.0/LICENSE`

 * *Files identical despite different names*

### Comparing `mutwo.midi-0.8.1/PKG-INFO` & `mutwo.midi-0.9.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mutwo.midi
-Version: 0.8.1
+Version: 0.9.0
 Summary: midi extension for event based framework mutwo
 Home-page: https://github.com/mutwo-org/mutwo.midi
 Author: Levin Eric Zimmermann
 Author-email: levin.eric.zimmermann@posteo.eu
 License: GPL
 Project-URL: Documentation, https://mutwo.readthedocs.io/en/latest/
 Requires-Python: >=3.9, <4
```

### Comparing `mutwo.midi-0.8.1/README.md` & `mutwo.midi-0.9.0/README.md`

 * *Files identical despite different names*

### Comparing `mutwo.midi-0.8.1/mutwo/midi_converters/backends.py` & `mutwo.midi-0.9.0/mutwo/midi_converters/backends.py`

 * *Files identical despite different names*

### Comparing `mutwo.midi-0.8.1/mutwo/midi_converters/constants.py` & `mutwo.midi-0.9.0/mutwo/midi_converters/constants.py`

 * *Files identical despite different names*

### Comparing `mutwo.midi-0.8.1/mutwo/midi_converters/frontends.py` & `mutwo.midi-0.9.0/mutwo/midi_converters/frontends.py`

 * *Files 1% similar despite different names*

```diff
@@ -169,29 +169,29 @@
     be rendered and how mutwo data shall be translated. This is necessary due
     to the limited and not always unambiguous nature of musical encodings in
     midi files. In this way the user can tweak the conversion routine to her
     or his individual needs.
 
     :param simple_event_to_pitch_list: Function to extract from a
         :class:`mutwo.core_events.SimpleEvent` a tuple that contains pitch objects
-        (objects that inherit from :class:`mutwo.ext.parameters.abc.Pitch`).
+        (objects that inherit from :class:`mutwo.music_parameters.abc.Pitch`).
         By default it asks the Event for its :attr:`pitch_list` attribute
-        (because by default :class:`mutwo.events.music.NoteLike` objects are expected).
+        (because by default :class:`mutwo.music_events.NoteLike` objects are expected).
         When using different Event classes than ``NoteLike`` with a different name for
         their pitch property, this argument should be overridden. If the function call
         raises an :obj:`AttributeError` (e.g. if no pitch can be extracted),
         mutwo will interpret the event as a rest.
     :type simple_event_to_pitch_list: typing.Callable[
             [core_events.SimpleEvent], tuple[music_parameters.abc.Pitch, ...]]
     :param simple_event_to_volume: Function to extract the volume from a
         :class:`mutwo.core_events.SimpleEvent` in the purpose of generating midi notes.
         The function should return an object that inhertis from
-        :class:`mutwo.ext.parameters.abc.Volume`. By default it asks the Event for
+        :class:`mutwo.music_parameters.abc.Volume`. By default it asks the Event for
         its :attr:`volume` attribute (because by default
-        :class:`mutwo.events.music.NoteLike` objects are expected).
+        :class:`mutwo.music_events.NoteLike` objects are expected).
         When using different Event classes than ``NoteLike`` with a
         different name for their volume property, this argument should be overridden.
         If the function call raises an :obj:`AttributeError` (e.g. if no volume can be
         extracted), mutwo will interpret the event as a rest.
     :type simple_event_to_volume: typing.Callable[
             [core_events.SimpleEvent], music_parameters.abc.Volume]
     :param simple_event_to_control_message_tuple: Function to generate midi control messages
@@ -216,20 +216,20 @@
         If set to ``True`` each :class:`~mutwo.core_events.SequentialEvent`
         only makes use of exactly n_midi_channel (see next parameter).
         If set to ``False`` each converted :class:`SequentialEvent` is allowed to make use of all
         available channels. If set to ``True`` and the amount of necessary MidiTracks is
         higher than the amount of available channels, mutwo will silently cycle through
         the list of available midi channel.
     :type distribute_midi_channels: bool
-    :param n_midi_channels_per_track: This parameter is only relevant for
+    :param midi_channel_count_per_track: This parameter is only relevant for
         distribute_midi_channels == True. It sets how many midi channels are assigned
         to one SequentialEvent. If microtonal chords shall be played by
         one SequentialEvent (via pitch bending messages) a higher number than 1 is
         recommended. Defaults to 1.
-    :type n_midi_channels_per_track: int
+    :type midi_channel_count_per_track: int
     :param mutwo_pitch_to_midi_pitch: class to convert from mutwo pitches
         to midi pitches. Default to :class:`MutwoPitchToMidiPitch`.
     :type mutwo_pitch_to_midi_pitch: :class:`MutwoPitchToMidiPitch`
     :param ticks_per_beat: Sets the timing precision of the midi file. From the mido
         documentation: "Typical values range from 96 to 480 but some use even more
         ticks per beat".
     :type ticks_per_beat: int
@@ -239,19 +239,19 @@
         value of mutwo is 120 BPM (this is also the value that is assumed by any
         midi-file-reading-software if no tempo has been specified). Tempo changes
         are supported (and will be written to the resulting midi file).
     :type tempo_envelope: core_events.TempoEnvelope
 
     **Example**:
 
-    >>> from mutwo.converters.frontends import midi
-    >>> from mutwo.ext.parameters import pitches
+    >>> from mutwo import midi_converters
+    >>> from mutwo import music_parameters
     >>> # midi file converter that assign a middle c to all events
-    >>> midi_converter = midi.EventToMidiFile(
-    >>>     simple_event_to_pitch_list=lambda event: (pitches.WesternPitch('c'),)
+    >>> midi_converter = midi_converters.EventToMidiFile(
+    >>>     simple_event_to_pitch_list=lambda event: (music_parameters.WesternPitch('c'),)
     >>> )
 
     **Disclaimer**:
         The current implementation doesn't support glissandi yet (only static pitches),
         time-signatures (the written time signature is always 4/4 for now) and
         dynamically changing tempo (ritardando or accelerando).
     """
@@ -268,15 +268,15 @@
         ] = music_converters.SimpleEventToVolume(),  # type: ignore
         simple_event_to_control_message_tuple: typing.Callable[
             [core_events.SimpleEvent], tuple[mido.Message, ...]
         ] = SimpleEventToControlMessageTuple(),
         midi_file_type: int = None,
         available_midi_channel_tuple: tuple[int, ...] = None,
         distribute_midi_channels: bool = False,
-        n_midi_channels_per_track: typing.Optional[int] = None,
+        midi_channel_count_per_track: typing.Optional[int] = None,
         mutwo_pitch_to_midi_pitch: MutwoPitchToMidiPitch = MutwoPitchToMidiPitch(),
         ticks_per_beat: typing.Optional[int] = None,
         instrument_name: typing.Optional[str] = None,
         tempo_envelope: typing.Optional[core_events.TempoEnvelope] = None,
     ):
         # TODO(find a less redundant way of setting default values)
         # set current default values if ext_parameters aren't defined
@@ -284,17 +284,17 @@
             midi_file_type = midi_converters.configurations.DEFAULT_MIDI_FILE_TYPE
 
         if available_midi_channel_tuple is None:
             available_midi_channel_tuple = (
                 midi_converters.configurations.DEFAULT_AVAILABLE_MIDI_CHANNEL_TUPLE
             )
 
-        if n_midi_channels_per_track is None:
-            n_midi_channels_per_track = (
-                midi_converters.configurations.DEFAULT_N_MIDI_CHANNELS_PER_TRACK
+        if midi_channel_count_per_track is None:
+            midi_channel_count_per_track = (
+                midi_converters.configurations.DEFAULT_MIDI_CHANNEL_COUNT_PER_TRACK
             )
 
         if ticks_per_beat is None:
             ticks_per_beat = midi_converters.configurations.DEFAULT_TICKS_PER_BEAT
 
         if instrument_name is None:
             instrument_name = (
@@ -315,15 +315,15 @@
         self._simple_event_to_pitch_list = simple_event_to_pitch_list
         self._simple_event_to_volume = simple_event_to_volume
         self._simple_event_to_control_message_tuple = (
             simple_event_to_control_message_tuple
         )
 
         self._distribute_midi_channels = distribute_midi_channels
-        self._n_midi_channels_per_track = n_midi_channels_per_track
+        self._midi_channel_count_per_track = midi_channel_count_per_track
         self._available_midi_channel_tuple = available_midi_channel_tuple
         self._midi_file_type = midi_file_type
         self._mutwo_pitch_to_midi_pitch = mutwo_pitch_to_midi_pitch
         self._ticks_per_beat = ticks_per_beat
         self._instrument_name = instrument_name
 
         self._tempo_envelope = tempo_envelope
@@ -442,15 +442,15 @@
         if self._distribute_midi_channels:
             available_midi_channel_tuple_cycle = itertools.cycle(
                 self._available_midi_channel_tuple
             )
             available_midi_channel_tuple_per_sequential_event = tuple(
                 tuple(
                     next(available_midi_channel_tuple_cycle)
-                    for _ in range(self._n_midi_channels_per_track)
+                    for _ in range(self._midi_channel_count_per_track)
                 )
                 for _ in simultaneous_event
             )
 
         else:
             available_midi_channel_tuple_per_sequential_event = tuple(
                 self._available_midi_channel_tuple for _ in simultaneous_event
@@ -617,15 +617,15 @@
     ) -> tuple[mido.Message, ...]:
         """Generates pitch-bend / note-on / note-off messages for each tone in a chord.
 
         Concatenates the midi messages for every played tone with the global control
         messages.
 
         Gets as an input relevant data for midi message generation that has been
-        extracted from a :class:`mutwo.abc.Event` object.
+        extracted from a :class:`mutwo.core_events.abc.Event` object.
         """
 
         absolute_tick_start = self._beats_to_ticks(absolute_time)
         absolute_tick_end = absolute_tick_start + self._beats_to_ticks(duration)
         velocity = volume.midi_velocity
 
         midi_message_list = []
@@ -677,33 +677,26 @@
         ):
             try:
                 extracted_data_list.append(extraction_function(simple_event))
             except AttributeError:
                 is_rest = True
                 break
 
-        print(extracted_data_list)
-
         # if not all relevant data could be extracted, simply ignore the
         # event
         if is_rest:
             return tuple([])
 
         # otherwise generate midi messages from the extracted data
         midi_message_tuple = self._extracted_data_to_midi_message_tuple(
             absolute_time,
             simple_event.duration,
             available_midi_channel_tuple_cycle,
             *extracted_data_list,  # type: ignore
         )
-        print(midi_message_tuple)
-        try:
-            print(midi_message_tuple[0].note)
-        except Exception:
-            pass
         return midi_message_tuple
 
     def _sequential_event_to_midi_message_tuple(
         self,
         sequential_event: core_events.SequentialEvent[
             typing.Union[core_events.SimpleEvent, core_events.SequentialEvent]
         ],
@@ -769,15 +762,18 @@
         sorted_midi_message_list = sorted(
             midi_message_tuple, key=lambda message: message.time
         )
 
         # add end of track message
         duration_in_ticks = self._beats_to_ticks(duration)
         sorted_midi_message_list.append(
-            mido.MetaMessage("end_of_track", time=duration_in_ticks)
+            mido.MetaMessage(
+                "end_of_track",
+                time=max((sorted_midi_message_list[-1].time, duration_in_ticks)),
+            )
         )
 
         # convert from absolute to relative time
         delta_tick_per_message_tuple = tuple(
             message1.time - message0.time
             for message0, message1 in zip(
                 sorted_midi_message_list, sorted_midi_message_list[1:]
@@ -870,15 +866,15 @@
                 )
             )
             midi_file.tracks.extend(midi_track_iterator)
 
     def _event_to_midi_file(
         self, event_to_convert: ConvertableEventUnion
     ) -> mido.MidiFile:
-        """Convert mutwo event object to mido MidiFile object."""
+        """Convert mutwo event object to mido `MidiFile` object."""
 
         midi_file = mido.MidiFile(
             ticks_per_beat=self._ticks_per_beat, type=self._midi_file_type
         )
 
         # depending on the event types timing structure different methods are called
         if isinstance(event_to_convert, core_events.SimultaneousEvent):
@@ -897,52 +893,65 @@
 
         return midi_file
 
     # ###################################################################### #
     #               public methods for interaction with the user             #
     # ###################################################################### #
 
-    def convert(self, event_to_convert: ConvertableEventUnion, path: str) -> None:
+    def convert(
+        self, event_to_convert: ConvertableEventUnion, path: typing.Optional[str] = None
+    ) -> mido.MidiFile:
         """Render a Midi file to the converters path attribute from the given event.
 
         :param event_to_convert: The given event that shall be translated
             to a Midi file.
         :type event_to_convert: typing.Union[core_events.SimpleEvent, core_events.SequentialEvent[core_events.SimpleEvent], core_events.SimultaneousEvent[core_events.SequentialEvent[core_events.SimpleEvent]]]
-        :param path: where to write the midi file. The typical file type extension '.mid'
-            is recommended, but not mandatory.
-        :type path: str
+        :param path: If this is a string the method will write a midi
+            file to the given path. The typical file type extension '.mid'
+            is recommended, but not mandatory. If set to `None` the
+            method won't write a midi file to the disk, but it will simply
+            return a :class:`mido.MidiFile` object. Default to `None`.
+        :type path: typing.Optional[str]
 
         The following example generates a midi file that contains a simple ascending
         pentatonic scale:
 
-        >>> from mutwo.events import basic, music
-        >>> from mutwo.ext.parameters import pitches
-        >>> from mutwo.converters.frontends import midi
-        >>> ascending_scale = basic.SequentialEvent(
+        >>> from mutwo import core_events
+        >>> from mutwo import music_events
+        >>> from mutwo import music_parameters
+        >>> from mutwo import midi_converters
+        >>> ascending_scale = core_events.SequentialEvent(
         >>>     [
-        >>>         music.NoteLike(pitches.WesternPitch(pitch), duration=1, volume=0.5)
+        >>>         music_events.NoteLike(music_parameters.WesternPitch(pitch), duration=1, volume=0.5)
         >>>         for pitch in 'c d e g a'.split(' ')
         >>>     ]
         >>> )
-        >>> midi_converter = midi.EventToMidiFile(
+        >>> midi_converter = midi_converters.EventToMidiFile(
         >>>     available_midi_channel_tuple=(0,)
         >>> )
         >>> midi_converter.convert(ascending_scale, 'ascending_scale.mid')
 
         **Disclaimer:** when passing nested structures, make sure that the
         nested object matches the expected type. Unlike other mutwo
-        converter classes (like :class:`mutwo.converters.core_converters.TempoConverter`)
+        converter classes (like :class:`mutwo.core_converters.TempoConverter`)
         :class:`EventToMidiFile` can't convert infinitely nested structures
         (due to the particular way how Midi files are defined). The deepest potential
         structure is a :class:`mutwo.core_events.SimultaneousEvent` (representing
         the complete MidiFile) that contains :class:`mutwo.core_events.SequentialEvent`
         (where each ``SequentialEvent`` represents one MidiTrack) that contains
         :class:`mutwo.core_events.SimpleEvent` (where each ``SimpleEvent``
         represents one midi note). If only one ``SequentialEvent`` is send,
         this ``SequentialEvent`` will be read as one MidiTrack in a MidiFile.
         If only one ``SimpleEvent`` get passed, this ``SimpleEvent`` will be
         interpreted as one MidiEvent (note_on and note_off) inside one
         MidiTrack inside one MidiFile.
         """
 
         midi_file = self._event_to_midi_file(event_to_convert)
-        midi_file.save(filename=path)
+
+        if path is not None:
+            try:
+                midi_file.save(filename=path)
+            except:
+                raise AssertionError(midi_file)
+
+        return midi_file
```

### Comparing `mutwo.midi-0.8.1/mutwo.midi.egg-info/PKG-INFO` & `mutwo.midi-0.9.0/mutwo.midi.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mutwo.midi
-Version: 0.8.1
+Version: 0.9.0
 Summary: midi extension for event based framework mutwo
 Home-page: https://github.com/mutwo-org/mutwo.midi
 Author: Levin Eric Zimmermann
 Author-email: levin.eric.zimmermann@posteo.eu
 License: GPL
 Project-URL: Documentation, https://mutwo.readthedocs.io/en/latest/
 Requires-Python: >=3.9, <4
```

### Comparing `mutwo.midi-0.8.1/setup.py` & `mutwo.midi-0.9.0/setup.py`

 * *Files identical despite different names*

