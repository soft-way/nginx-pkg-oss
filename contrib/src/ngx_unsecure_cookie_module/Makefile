
# ngx_unsecure_cookie_module

include $(dir $(abspath $(lastword $(MAKEFILE_LIST))))/version
UNSECURE_COOKIE_MODULE_URL := $(GITHUB)/soft-way/nginx_unsecure_cookie_module/archive/v$(UNSECURE_COOKIE_NGINX_MODULE_VERSION).tar.gz

PKGS += ngx_unsecure_cookie_module

$(TARBALLS)/ngx_unsecure_cookie_module-$(UNSECURE_COOKIE_NGINX_MODULE_VERSION).tar.gz:
	$(call download_pkg,$(UNSECURE_COOKIE_MODULE_URL),ngx_unsecure_cookie_module)

.sum-ngx_unsecure_cookie_module: ngx_unsecure_cookie_module-$(UNSECURE_COOKIE_NGINX_MODULE_VERSION).tar.gz

ngx_unsecure_cookie_module: ngx_unsecure_cookie_module-$(UNSECURE_COOKIE_NGINX_MODULE_VERSION).tar.gz .sum-ngx_unsecure_cookie_module
	$(UNPACK)
	$(MOVE)

.ngx_unsecure_cookie_module: ngx_unsecure_cookie_module
	touch $@

