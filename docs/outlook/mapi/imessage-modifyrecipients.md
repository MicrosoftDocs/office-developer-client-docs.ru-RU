---
title: IMessageModifyRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.ModifyRecipients
api_type:
- COM
ms.assetid: 2625f29d-325f-417d-bcec-49d580f9cd7e
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 3edcef69880dbc2a566a44582113c43802a47324
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809272"
---
# <a name="imessagemodifyrecipients"></a>IMessage::ModifyRecipients

  
  
**Относится к**: Outlook 
  
����������, �������� ��� �������� ����������� ���������.
  
```cpp
HRESULT ModifyRecipients(
  ULONG ulFlags,
  LPADRLIST lpMods
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ������� ����� �����, ������� ��������� ����������� ���������. ���� ��� ���������  _ulFlags_ ���������� ����, **ModifyRecipients** �������� ��� ������������ ����������� ������ �����������, �� ������� ��������� ��������  _lpMods_. ��������� ����� ����� ������ ���  _ulFlags_:
    
MODRECIP_ADD 
  
> ����������, �� ������� ��������� ��������  _lpMods_ ������� �������� � ������ �����������. 
    
MODRECIP_MODIFY 
  
> ����������, �� ������� ��������� ��������  _lpMods_ ���������� �������� ������������ �����������. ��� ������������ �������� ���������� �������� �������� ��������������� ��������� [ADRENTRY](adrentry.md) . 
    
MODRECIP_REMOVE 
  
> Текущих получателей необходимо удалить из списка получателей, используя в качестве индекса свойство **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)), включенные в массив значений свойств каждого получателя записи с помощью параметра _lpMods_ . 
    
 _lpMods_
  
> [in] ��������� �� ��������� [ADRLIST](adrlist.md) , ������� �������� ������ �����������, ����� ���� ���������, ������� ��� �������� � ���������. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ��������� ������ ����������� ��������� �������.
    
## <a name="remarks"></a>���������

����� **IMessage::ModifyRecipients** �������� ������ ����������� ���������. ��� �� ����� ������, ������� ���������� � ��������� [ADRLIST](adrlist.md) , ��� ����������� ����������. 
  
��������� **ADRLIST** �������� ���� ��������� [ADRENTRY](adrentry.md) ��� ������� ����������, � ������ **ADRENTRY** ��������� �������� ������ �������� �������, ����������� ���������� ����������. 
  
������ ����������� � ��������� **ADRLIST** ����� ��������� ��� ���������. ������� ����������� � ����� � ���� ��������, ������� ��������. Неизвестный получатель содержит только свойства **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) и **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), а Разрешить получателя эти два свойства, а также **PR_ADDRTYPE **([PidTagAddressType](pidtagaddresstype-canonical-property.md)) и **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Если доступен **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), он может быть включен также.
  
����� �������� ��������� ��� ���������� �������� ������ ����������� ���������� ����������� � ��� ������ �����������. ���������� ����������� ������� ����� � ���������� ��� ������ � ��������� ��������� ����������� ���������. �������������� �������� � �������� ���������� ���� � ����� ������ ������� [������������� ����](resolving-a-recipient-name.md)��. ��� ��������� �������������� �������� � ����� ������ ������� � �������� ����� ������ [���������� ���������� ����](implementing-name-resolution.md).
  
� ���������� � ����������� ���������� � ���������� ����������� ���������� ����� ���� NULL. ���� **cValues** ��������� **ADRENTRY** ��� ���������� ������������� ������� �������� � ���� **rgPropVals** ����� �������� NULL. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

����� ������� ������ �����������, ������ [IAddrBook::Address](imapisupport-address.md) ��� ����������� ����������� ���������� ����� � ���������� ������������ ������� ��������. ������ �������, ��������� ��������  _lppAdrList_ ��� **Address** ����� ���� ������� **ModifyRecipients** ��� ��������  _lpMods_. 
  
��� �������� �������� ��� ���������� � ��������� [ADRLIST](adrlist.md) �������� ��� �������� ����������, �� ������ �� ��� ����� ��� ����������. ��� ��������� ����������, ��������� ��� ��������, �� ���������� � ��������� **ADRLIST**. ��� ��������� �������� ������ ������� ��� ���� ����������� ���������, �������� [GetRecipientTable](imessage-getrecipienttable.md) � �������� ��� ������. ��������� � ��������� ��������� **ADRLIST** **SRowSet**, �� ����� ������������ �����������.
  
 **ModifyRecipients** �������� ��� ������ � ������� ������ ����������� ��������, �� ������� ���������  _lpMods_ ���� �� ���� �� ������ �������� � ������� ���������  _ulFlags_. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

��� ��������� ����� MODRECIP_MODIFY **ModifyRecipients** �������� ������� ���������� ������ ����� � ��������� [ADRLIST](adrlist.md) ���������� �  _lpMods_. ������� �� ��� ������� ��� ��������, ������� ������ ����� ���������� ���������� �� ����, �������� �� ��� ���� �������� ��� �������������� ���������� ��������.
  
���� ����������� ��������� ������� ��� ��������� ������� ����������� � ��������� **ADRLIST**. 
  
- �� ����������� PT_NULL � �������� ���� ��������. **ModifyRecipients** ���������� ������ ��� ����������� ��� ��������. 
    
- �� ����������� PT_ERROR � �������� ���� ��������. **ModifyRecipients** ���������� ��� ��������. 
    
- �������� �������� **PR_ROWID** ��� ���� �����������, ��������� ����� MODRECIP_REMOVE ��� MODRECIP_MODIFY �  _ulFlags_. 
    
- �� ��������� �������� **PR_ROWID** ��� �����-���� �� ����������� �� ����� ���� MODRECIP_ADD �  _ulFlags_ ��� ��� �������� ���� �  _ulFlags_.
    
���� �������� �������� **PR_ADDRTYPE** ��� �������� **PR_EMAIL_ADDRESS** ��� ����������, � ������ ��� ��� ��� ��������, �� ������������� ��� ������ � ����� ����������, ��� ���������� � **PR_ENTRYID**, ���������� �� ����������. �� ���� ���������� ��� ��������, � ����������� �� ���������� �����.
  
- ��������� ������������ �� �����, ������������ �������� **PR_ADDRTYPE** � **PR_EMAIL_ADDRESS**. 
    
- ��������� ����� ���������� ����������, ������������ ��������� **PR_ENTRYID**.
    
- ��������� ����� ��������� �������������� ��-�� ���������������� �������� �� ������.
    
������������� ������� �������������, ��������� � [������ ADRLIST � SRowSet ��������](managing-memory-for-adrlist-and-srowset-structures.md) ��� ��������� ������ ��� ������ �����������. **ModifyRecipients** �� ����������� ��������� **ADRLIST** �� ����� -���� �� �� ��������� ���������. ��������� **ADRLIST** � ������� [SPropValue](spropvalue.md) ��������� ���������� �������� �������� � ������� ������� [MAPIAllocateBuffer](mapiallocatebuffer.md) ����� �������, ����� ���������� ������� �� �����������. ���� ����� ������� ��������������� ����� �� ����� ��� ������ **SPropValue** ���������, ��� ����� �������� ��������� **SPropValue** ��� ����� ���������� ����� ������� ������ � ������� [MAPIFreeBuffer](mapifreebuffer.md). �������� ��������� **SPropValue** ����� ����� ���������� � ������� **MAPIFreeBuffer**.
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |Mfcmapi (en) ����� **IMessage::ModifyRecipients** ������������ ��� ���������� ����� ����������� �� ���������.  <br/> |
   
## <a name="see-also"></a>��. �����



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

