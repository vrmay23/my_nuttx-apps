############################################################################
# apps/logging/nxscope/Makefile
#
# SPDX-License-Identifier: Apache-2.0
#
# Licensed to the Apache Software Foundation (ASF) under one or more
# contributor license agreements.  See the NOTICE file distributed with
# this work for additional information regarding copyright ownership.  The
# ASF licenses this file to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance with the
# License.  You may obtain a copy of the License at
#
#   http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
# WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  See the
# License for the specific language governing permissions and limitations
# under the License.
#
############################################################################

include $(APPDIR)/Make.defs

# NxScope Library

CSRCS = nxscope.c nxscope_chan.c nxscope_internals.c

ifeq ($(CONFIG_LOGGING_NXSCOPE_INTF_SERIAL),y)
CSRCS += nxscope_iser.c
endif

ifeq ($(CONFIG_LOGGING_NXSCOPE_INTF_DUMMY),y)
CSRCS += nxscope_idummy.c
endif

ifeq ($(CONFIG_LOGGING_NXSCOPE_PROTO_SER),y)
CSRCS += nxscope_pser.c
endif

include $(APPDIR)/Application.mk
