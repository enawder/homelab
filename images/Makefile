.POSIX:

output = output

oses = $(notdir $(realpath $(wildcard */.)))
templates = $(wildcard */template.json)
output_images = $(foreach os, $(oses), $(os)/$(output))
output_manifests = $(foreach image, $(output_images), $(image)/manifest.json)

all: $(oses)

%/$(output)/manifest.json: %/template.json
	@rm -rf $(dir $@)
	@mkdir -p $(dir $@)
	@PACKER_LOG=1 \
	PACKER_LOG_PATH=$(dir $@)/packer.log \
	packer build -timestamp-ui $<

define os_target
.PHONY: $(1)
$(1): $(1)/$(output)/manifest.json
endef
$(foreach os, $(oses), $(eval $(call os_target, $(os))))
