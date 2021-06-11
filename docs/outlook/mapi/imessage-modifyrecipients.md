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
ms.openlocfilehash: 07e1c2104068a6eb242e8ba81f91655edaa92cd8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426242"
---
# <a name="imessagemodifyrecipients"></a>IMessage::ModifyRecipients

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
����������, �������� ��� �������� ����������� ���������.
  
```cpp
HRESULT ModifyRecipients(
  ULONG ulFlags,
  LPADRLIST lpMods
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] ������� ����� �����, ������� ��������� ����������� ���������. ���� ��� ���������  _ulFlags_ ���������� ����, **ModifyRecipients** �������� ��� ������������ ����������� ������ �����������, �� ������� ��������� ��������  _lpMods_. ��������� ����� ����� ������ ���  _ulFlags_:
    
MODRECIP_ADD 
  
> ����������, �� ������� ��������� ��������  _lpMods_ ������� �������� � ������ �����������. 
    
MODRECIP_MODIFY 
  
> ����������, �� ������� ��������� ��������  _lpMods_ ���������� �������� ������������ �����������. ��� ������������ �������� ���������� �������� �������� ��������������� ��������� [ADRENTRY](adrentry.md) . 
    
MODRECIP_REMOVE 
  
> Существующие получатели должны быть удалены из списка **получателей, используя** в качестве индекса свойство PR_ROWID [(PidTagRowid),](pidtagrowid-canonical-property.md)включенное в массив значений свойств каждой записи получателя в _параметре lpMods._ 
    
 _lpMods_
  
> [in] ��������� �� ��������� [ADRLIST](adrlist.md) , ������� �������� ������ �����������, ����� ���� ���������, ������� ��� �������� � ���������. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ��������� ������ ����������� ��������� �������.
    
## <a name="remarks"></a>Примечания

����� **IMessage::ModifyRecipients** �������� ������ ����������� ���������. ��� �� ����� ������, ������� ���������� � ��������� [ADRLIST](adrlist.md) , ��� ����������� ����������. 
  
��������� **ADRLIST** �������� ���� ��������� [ADRENTRY](adrentry.md) ��� ������� ����������, � ������ **ADRENTRY** ��������� �������� ������ �������� �������, ����������� ���������� ����������. 
  
������ ����������� � ��������� **ADRLIST** ����� ��������� ��� ���������. ������� ����������� � ����� � ���� ��������, ������� ��������. Неурегулированный получатель содержит только **свойства PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)и **PR_RECIPIENT_TYPE** [(PidTagRecipientType),](pidtagrecipienttype-canonical-property.md)а разрешенный получатель содержит эти два свойства плюс **PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)и **PR_ENTRYID** [(PidTagEntryId).](pidtagentryid-canonical-property.md) Если **PR_EMAIL_ADDRESS** [(PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)доступен, он также может быть включен.
  
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
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**�����������**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |Mfcmapi (en) ����� **IMessage::ModifyRecipients** ������������ ��� ���������� ����� ����������� �� ���������.  <br/> |
   
## <a name="see-also"></a>См. также



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

