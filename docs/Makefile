SRCDIR = $(realpath .)

include $(TOPDIR)/src/include/deprecated.mk
include $(TOPDIR)/src/include/version.mk
include $(TOPDIR)/src/include/rules.mk
include $(TOPDIR)/src/include/defaults.mk

MAN1TARGETS = efisecdb.1 \
	      efivar.1

MAN3TARGETS = efi_append_variable.3 \
	     efi_del_variable.3 \
	     efi_get_next_variable_name.3 \
	     efi_get_variable.3 \
	     efi_get_variable_attributes.3 \
	     efi_get_variable_size.3 \
	     efi_guid_to_id_guid.3 \
	     efi_guid_to_name.3 \
	     efi_guid_to_str.3 \
	     efi_guid_to_symbol.3 \
	     efi_name_to_guid.3 \
	     efi_set_variable.3 \
	     efi_str_to_guid.3 \
	     efi_symbol_to_guid.3 \
	     efi_variables_supported.3 \
	     efi_variable_t.3 \
	     efi_variable_import.3 \
	     efi_variable_export.3 \
	     efi_variable_alloc.3 \
	     efi_variable_free.3 \
	     efi_variable_set_name.3 \
	     efi_variable_get_name.3 \
	     efi_variable_set_guid.3 \
	     efi_variable_get_guid.3 \
	     efi_variable_set_data.3 \
	     efi_variable_get_data.3 \
	     efi_variable_get_attributes.3 \
	     efi_variable_set_attributes.3 \
	     efi_variable_realize.3

all : $(MAN1TARGETS) $(MAN3TARGETS)

clean :
	@rm -f efisecdb.1

prep :

test :

install : $(MAN1TARGETS) $(MAN3TARGETS)
	$(INSTALL) -d -m 755 $(DESTDIR)$(MANDIR)/man1
	$(foreach x, $(MAN1TARGETS), $(INSTALL) -m 644 $(x) $(DESTDIR)/$(MANDIR)/man1/;)
	$(INSTALL) -d -m 755 $(DESTDIR)$(MANDIR)/man3
	$(foreach x, $(MAN3TARGETS), $(INSTALL) -m 644 $(x) $(DESTDIR)/$(MANDIR)/man3/;)

.PHONY: all clean install

include $(TOPDIR)/src/include/rules.mk
