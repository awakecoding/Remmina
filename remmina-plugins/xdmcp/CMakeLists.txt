# remmina-plugin-xdmcp - The GTK+ Remote Desktop Client
#
# Copyright (C) 2011 Marc-Andre Moreau
#
# This program is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; either version 2 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 59 Temple Place, Suite 330, 
# Boston, MA 02111-1307, USA.

set(REMMINA_PLUGIN_XDMCP_SRCS
	remminapluginxdmcp.c
	)

add_library(remmina-plugin-xdmcp ${REMMINA_PLUGIN_XDMCP_SRCS})
set_target_properties(remmina-plugin-xdmcp PROPERTIES PREFIX "")

include_directories(${REMMINA_COMMON_INCLUDE_DIRS})
target_link_libraries(remmina-plugin-xdmcp ${REMMINA_COMMON_LIBRARIES})

install(TARGETS remmina-plugin-xdmcp DESTINATION ${REMMINA_PLUGINDIR})

install(FILES 16x16/emblems/remmina-xdmcp-ssh.png 16x16/emblems/remmina-xdmcp.png DESTINATION ${APPICON16_EMBLEMS_DIR})
install(FILES 22x22/emblems/remmina-xdmcp-ssh.png 22x22/emblems/remmina-xdmcp.png DESTINATION ${APPICON22_EMBLEMS_DIR})
