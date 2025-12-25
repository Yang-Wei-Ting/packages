# Copyright (C) 2025 Wei-Ting Yang <williamatcg@gmail.com>
#
# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=thrift
PKG_VERSION:=0.22.0
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=@APACHE/$(PKG_NAME)/$(PKG_VERSION)
PKG_HASH:=794a0e455787960d9f27ab92c38e34da27e8deeda7a5db0e59dc64a00df8a1e5

PKG_MAINTAINER:=Wei-Ting Yang <williamatcg@gmail.com>
PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=LICENSE
PKG_CPE_ID:=cpe:/a:apache:thrift

PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/thrift
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=Apache Thrift
  DEPENDS:=
  URL:=https://thrift.apache.org/
endef

define Package/thrift/description
The Apache Thrift software framework, for scalable cross-language services
development, combines a software stack with a code generation engine to build
services that work efficiently and seamlessly between C++, Java, Python, PHP,
Ruby, Erlang, Perl, Haskell, C#, Cocoa, JavaScript, Node.js, Smalltalk, OCaml
and Delphi and other languages.
endef

CMAKE_OPTIONS += \
	-DBUILD_JAVASCRIPT=OFF \
	-DBUILD_NODEJS=OFF \
	-DBUILD_SHARED_LIBS=ON \
	-DBUILD_TESTING=ON \
	-DBUILD_TUTORIALS=ON \
	-DTHRIFT_COMPILER_CL=OFF \
	-DTHRIFT_COMPILER_D=OFF \
	-DTHRIFT_COMPILER_DART=OFF \
	-DTHRIFT_COMPILER_DELPHI=OFF \
	-DTHRIFT_COMPILER_ERL=OFF \
	-DTHRIFT_COMPILER_GO=OFF \
	-DTHRIFT_COMPILER_GV=OFF \
	-DTHRIFT_COMPILER_HAXE=OFF \
	-DTHRIFT_COMPILER_HTML=OFF \
	-DTHRIFT_COMPILER_JAVA=OFF \
	-DTHRIFT_COMPILER_JAVAME=OFF \
	-DTHRIFT_COMPILER_JS=OFF \
	-DTHRIFT_COMPILER_JSON=OFF \
	-DTHRIFT_COMPILER_KOTLIN=OFF \
	-DTHRIFT_COMPILER_LUA=OFF \
	-DTHRIFT_COMPILER_MARKDOWN=OFF \
	-DTHRIFT_COMPILER_NETSTD=OFF \
	-DTHRIFT_COMPILER_OCAML=OFF \
	-DTHRIFT_COMPILER_PERL=OFF \
	-DTHRIFT_COMPILER_PHP=OFF \
	-DTHRIFT_COMPILER_PY=OFF \
	-DTHRIFT_COMPILER_RB=OFF \
	-DTHRIFT_COMPILER_RS=OFF \
	-DTHRIFT_COMPILER_ST=OFF \
	-DTHRIFT_COMPILER_SWIFT=OFF \
	-DTHRIFT_COMPILER_XML=OFF \
	-DTHRIFT_COMPILER_XSD=OFF \
	-DWITH_JAVA=OFF \
	-DWITH_JAVASCRIPT=OFF \
	-DWITH_NODEJS=OFF

define Package/thrift/install
	true
endef

$(eval $(call BuildPackage,thrift))
