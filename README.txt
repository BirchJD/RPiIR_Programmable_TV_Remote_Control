# Copyright (C) 2019 Jason Birch
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <http://www.gnu.org/licenses/>.



Transmitting Data From A Raspberry Pi With An Infra Red LED
And Receiving The Data On Another Raspberry Pi With A VS1838B Infra Red Device
Recording TV, HiFi, Set-top box remote controls and playing back


Patreon, donations help produce more OpenSource projects:
https://www.patreon.com/_DevelopIT

Videos of this project:


Source Code on GitHub:
https://github.com/BirchJD/RPiIrTxRx_VS1838B



Applications
============

./PiIrTx.py
An example application to take an ASCII string as a command line argument,
which will then be transmitted as part of a data package. The data package
allows the data to be checked for validity on reception in case of
transmission/reception corruption. Demonstrates a basic encryption of the data
on transmission. The PiIrRx.py application can be used to receive and display
the unencrypted data. The data is transmitted on an infra red LED at 3KHz on a
carrier frequency of 38KHz so a VS1838B infra red receiver can receive the data.
e.g.
./PiIrTx.py 'Sending test message.'

./PiIrRx.py
An example application to receive validate, unencrypt and display a packet of
data transmitted from the PiIrTx.py application.

./PiIr.py
Start monitoring and logging data. To provide various views of the data being
received. Allowing analysis and identification of required data transmitted
on Infra Red. Also provides a noise count, which indicates how much local Infra
Red interference is being experienced, providing a method of locating the
device in a location with low interference noise, improving reliability of
data reception.

./PiIrRx_Data.py
Receive and record information from a remote control, such as TV, set-top box,
HiFi, etc. Which can be played back using the PiIrTx_Data.py script.

./PiIrTx_Data.py
Playback information recorded from PiIrRx_Data.py to control devices such as a
TV, set-top box, HiFi, etc. Examples can be found in the EXAMPLES directory.

