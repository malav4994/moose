HHChannelBase
-------------

.. py:class:: HHChannelBase

   HHChannelBase: Base class for Hodgkin-Huxley type voltage-gated Ion channels. Something like the old tabchannel from GENESIS, but also presents a similar interface as hhchan from GENESIS.

   .. py:method:: setXpower

      (*destination message field*)      Assigns field value.


   .. py:method:: getXpower

      (*destination message field*)      Requests field value. The requesting Element must provide a handler for the returned value.


   .. py:method:: setYpower

      (*destination message field*)      Assigns field value.


   .. py:method:: getYpower

      (*destination message field*)      Requests field value. The requesting Element must provide a handler for the returned value.


   .. py:method:: setZpower

      (*destination message field*)      Assigns field value.


   .. py:method:: getZpower

      (*destination message field*)      Requests field value. The requesting Element must provide a handler for the returned value.


   .. py:method:: setInstant

      (*destination message field*)      Assigns field value.


   .. py:method:: getInstant

      (*destination message field*)      Requests field value. The requesting Element must provide a handler for the returned value.


   .. py:method:: setX

      (*destination message field*)      Assigns field value.


   .. py:method:: getX

      (*destination message field*)      Requests field value. The requesting Element must provide a handler for the returned value.


   .. py:method:: setY

      (*destination message field*)      Assigns field value.


   .. py:method:: getY

      (*destination message field*)      Requests field value. The requesting Element must provide a handler for the returned value.


   .. py:method:: setZ

      (*destination message field*)      Assigns field value.


   .. py:method:: getZ

      (*destination message field*)      Requests field value. The requesting Element must provide a handler for the returned value.


   .. py:method:: setUseConcentration

      (*destination message field*)      Assigns field value.


   .. py:method:: getUseConcentration

      (*destination message field*)      Requests field value. The requesting Element must provide a handler for the returned value.


   .. py:method:: concen

      (*destination message field*)      Incoming message from Concen object to specific conc to usein the Z gate calculations


   .. py:method:: createGate

      (*destination message field*)      Function to create specified gate.Argument: Gate type [X Y Z]


   .. py:method:: setNumGateX

      (*destination message field*)      Assigns number of field entries in field array.


   .. py:method:: getNumGateX

      (*destination message field*)      Requests number of field entries in field array.The requesting Element must provide a handler for the returned value.


   .. py:method:: setNumGateY

      (*destination message field*)      Assigns number of field entries in field array.


   .. py:method:: getNumGateY

      (*destination message field*)      Requests number of field entries in field array.The requesting Element must provide a handler for the returned value.


   .. py:method:: setNumGateZ

      (*destination message field*)      Assigns number of field entries in field array.


   .. py:method:: getNumGateZ

      (*destination message field*)      Requests number of field entries in field array.The requesting Element must provide a handler for the returned value.


   .. py:attribute:: Xpower

      double (*value field*)      Power for X gate


   .. py:attribute:: Ypower

      double (*value field*)      Power for Y gate


   .. py:attribute:: Zpower

      double (*value field*)      Power for Z gate


   .. py:attribute:: instant

      int (*value field*)      Bitmapped flag: bit 0 = Xgate, bit 1 = Ygate, bit 2 = ZgateWhen true, specifies that the lookup table value should beused directly as the state of the channel, rather than usedas a rate term for numerical integration for the state


   .. py:attribute:: X

      double (*value field*)      State variable for X gate


   .. py:attribute:: Y

      double (*value field*)      State variable for Y gate


   .. py:attribute:: Z

      double (*value field*)      State variable for Y gate


   .. py:attribute:: useConcentration

      int (*value field*)      Flag: when true, use concentration message rather than Vm tocontrol Z gate
