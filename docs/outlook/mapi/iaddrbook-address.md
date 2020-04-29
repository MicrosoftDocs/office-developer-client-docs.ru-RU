---
title: иаддрбукаддресс
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Address
api_type:
- COM
ms.assetid: ef2112c7-35cd-4106-ad18-a45e1dbe07d6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c2546fc990169526361f2c452c50212123d8284d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407909"
---
# <a name="iaddrbookaddress"></a>IAddrBook::Address

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Отображает диалоговое окно "Адресная книга Outlook". 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Параметры

 _лпулуипарам_
  
> [вход, выход] Указатель на дескриптор родительского окна диалогового окна. Во входных данных дескриптор окна всегда должен быть передан. В выходных данных, если для члена **ulFlags** параметра _лпадрпармс_ задано значение DIALOG_SDI, возвращается дескриптор окна немодального диалогового окна. См. раздел "Замечания". 
    
 _лпадрпармс_
  
> [вход, выход] Указатель на структуру [адрпарм](adrparm.md) , которая управляет представлением и поведением диалогового окна "адрес". 
    
 _лппадрлист_
  
> [вход, выход] Указатель на указатель на структуру [ADRLIST](adrlist.md) , содержащую сведения о получателе. В параметре input этот параметр может иметь значение NULL или указывать на допустимый указатель. В выходных данных этот параметр указывает на указатель на допустимые сведения о получателе. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Успешно отображено диалоговое окно Common Address.
    
## <a name="remarks"></a>Примечания

Если элемент **ulFlags** параметра _лпадрпармс_ имеет значение DIALOG_SDI, ожидая возврата дескриптора окна немодального диалогового окна на выходе, оно игнорируется в Outlook; модальная версия диалогового окна всегда отображается в клиентах, не относящихся к Outlook. 
  
Структура **ADRLIST** , передаваемая через MAPI абоненту с помощью параметра _лппадрлист_ , содержит массив структур [адрентри](adrentry.md) , по одной структуре для каждого получателя. При передаче в метод [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md) исходящего сообщения в параметре _лпмодс_ структура **ADRLIST** может использоваться для обновления списка получателей. 
  
Каждая структура **адрентри** в структуре **ADRLIST** содержит ноль или более структур [спропвалуе](spropvalue.md) , одна структура для каждого набора свойств получателя. Если для удаления получателя используется диалоговое окно, представленное методом **Address** , может иметь нулевые структуры **спропвалуе** . При наличии одной или нескольких структур **спропвалуе** для добавления или обновления получателя используется соответствующая структура **адрентри** . Получатель может быть разрешен, что указывает на то, что одна из структур **спропвалуе** описывает свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) получателя или является неразрешенным, что указывает на отсутствие свойства **PR_ENTRYID** . 
  
Кроме **PR_ENTRYID**, разрешенные получатели включают следующие свойства:
  
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Структура **ADRLIST** , которую передает вызывающий абонент, может иметь другой размер из структуры, которую возвращает MAPI. Если MAPI должен вернуть более крупную структуру **ADRLIST** , он освобождает исходную структуру и выделяет новую. При выделении памяти для структуры **ADRLIST** выделяет память для каждой структуры **спропвалуе** отдельно. Дополнительные сведения о том, как распределять и освобождать структуры **ADRLIST** , приведены в статье [Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)
  
 **Адрес** немедленно возвращается, если установлен флаг DIALOG_SDI в элементе **ulFlags** структуры **адрпарм** в параметре _лпадрпармс_ . Флаг DIALOG_SDI игнорируется для клиентов, не относящихся к Outlook. Если DIALOG_SDI игнорируется, отображается модальная версия диалогового окна, и указатель на дескриптор не должен быть ожидаемым в _лпулуипарам_.
  
 **Address** поддерживает строки символов Юникода в структуре **адрпарм** , если AB_UNICODEUI был указан в элементе **ulFlags** элемента **адрпарм** в параметре _Лпадрпармс_ , и он поддерживает строки символов Юникода в **ADRLIST**. Строки Юникод преобразуются в формат многобайтовых символов (MBCS), прежде чем они будут отображаться в диалоговом окне Адресная книга Outlook.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Маписторефунктионс. cpp  <br/> |опеносерусерсмаилбоксфромгал  <br/> |MFCMAPI использует метод **Address** , позволяющий пользователю выбрать почтовый ящик, который нужно открыть.  <br/> |
   
## <a name="see-also"></a>См. также



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[ADRPARM](adrparm.md)
  
[FreePadrlist](freepadrlist.md)
  
[FreeProws](freeprows.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

