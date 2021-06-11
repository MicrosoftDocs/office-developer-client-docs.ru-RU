---
title: HrValidateIPMSubtree
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrValidateIPMSubtree
api_type:
- COM
ms.assetid: 6454c1fa-5216-4934-a908-48c634ac4a07
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6cf51985e534434c584eff4d63dfbf239121ee85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436575"
---
# <a name="hrvalidateipmsubtree"></a>HrValidateIPMSubtree

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Добавляет стандартные папки межличностных сообщений (IPM) в хранилище сообщений. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a>Parameters

 _lpMDB_
  
> [in] Указатель на объект магазина сообщений, к которому нужно добавить папки. 
    
 _ulFlags_
  
> [in] Bitmask флагов, используемых для управления тем, как создаются папки. Можно установить следующие флаги:
    
MAPI_FORCE_CREATE 
  
> Папки должны проверяться перед созданием, даже если свойства магазина сообщений указывают, что они допустимы. Обычно клиентская заявка задает этот флаг, если ошибка указывает на повреждение структуры существующей папки. 
    
MAPI_FULL_IPM_TREE 
  
> Полный набор папок IPM должен быть создан в корневой папке магазина сообщений. Названия папок в иерархии:
    
    - Представления папок
    
    - Общие представления
    
    - Корень поиска\*
    
    - Подтрий IPM\*
    
    - Inbox;
    
    - Исходящие
    
    - Удаленные элементы\*
    
    - Отправленные
    
    где отмечены три папки, это минимальный набор, созданный даже \* MAPI_FULL_IPM_TREE флага. Обычно клиентская заявка задает этот флаг, когда хранилище сообщений, в котором должны быть созданы папки, является хранилищем по умолчанию.
    
 _lpcValues_
  
> [in, out] Указатель на количество [структур SPropValue](spropvalue.md) в массиве, возвращаемом в _параметре lppProps._ Значение параметра  _lpcValues_ может быть нулевым, если  _lppProps_ является NULL. 
    
 _lppProps_
  
> [in, out] Указатель на указатель на массив структур **SPropValue,** содержащий значения свойств **для свойства PR_VALID_FOLDER_MASK** [(PidTagValidFolderMask)](pidtagvalidfoldermask-canonical-property.md)и для соответствующих свойств идентификатора записи папок. Если **HrValidateIPMSubtree** создает почтовый ящик в хранилище сообщений, массив **SPropValue** включает идентификатор входа в почтовый ящик со специальным тегом свойства под кодом  `PROP_TAG(PT_BINARY, PROP_ID_NULL)` . Параметр _lppProps_ может быть NULL, что указывает на то, что реализация вызовов не требует возврата **массива SPropValue.** 
    
 _lppMapiError_
  
> [вышел] Указатель на указатель на структуру [MAPIERROR,](mapierror.md) которая содержит сведения о версии, компоненте и контексте для ошибки. Параметр _lppMAPIError задан_ в NULL, если не возвращается структура **MAPIERROR.** 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

MAPI использует функцию **HrValidateIPMSubtree** для создания стандартного подтрия IPM в хранилище сообщений при первом открытие магазина или при изготовлении магазина по умолчанию. Эта функция также может использоваться клиентских приложений для проверки или ремонта стандартных папок сообщений. 
  
 **HrValidateIPMSubtree** всегда создает папки Root и IPM Subtree в корневой папке магазина и папку "Удаленные элементы" в папке Подтрия IPM. Папка подтриба IPM является корнем иерархии IPM в этом хранилище сообщений. Корневая папка поиска может использоваться в качестве корневого подтриба для папок результатов поиска. 
  
Клиенты IPM должны отображать свое представление папки, начиная с корневой папки подтрия IPM, и показывать под ней детские папки. Сведения в корневой папке магазина сообщений не должны отображаться в пользовательском интерфейсе клиента. Эта функция означает, что если клиент должен скрыть сведения, эти сведения можно поместить в корневой каталог IPM, где она не видна пользователю. Напротив, приложения, не вложенные в IPM, для которых сообщения и папки должны быть невидимыми для пользователя, например в серверном хранилище сообщений, могут выбрасывать их за пределы иерархии IPM. 
  
 **HrValidateIPMSubtree** задает  свойство PR_VALID_FOLDER_MASK, чтобы указать, имеет ли каждая создаваемая папка IPM допустимый идентификатор входа. Следующие свойства идентификатора записи в хранилище сообщений заданы идентификаторам записи соответствующих папок и возвращаются в _параметре lppProps_ вместе с **PR_VALID_FOLDER_MASK:** 
  
 **PR_COMMON_VIEWS_ENTRYID** [(PidTagCommonViewsEntryId)](pidtagcommonviewsentryid-canonical-property.md)
  
> **PR_FINDER_ENTRYID** [(PidTagFinderEntryId)](pidtagfinderentryid-canonical-property.md)
  
> **PR_IPM_OUTBOX_ENTRYID** [(PidTagIpmOutboxEntryId)](pidtagipmoutboxentryid-canonical-property.md)
  
> **PR_IPM_SENTMAIL_ENTRYID** [(PidTagIpmSentMailEntryId)](pidtagipmsentmailentryid-canonical-property.md)
  
> **PR_IPM_SUBTREE_ENTRYID** [(PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
  
> **PR_IPM_WASTEBASKET_ENTRYID** [(PidTagIpmWastebasketEntryId)](pidtagipmwastebasketentryid-canonical-property.md)
  
> **PR_VIEWS_ENTRYID** [(PidTagViewsEntryId)](pidtagviewsentryid-canonical-property.md)
  
> Местообладатель [PROP_TAG](prop_tag.md) для почтового ящика IPM (PT_BINARY, PROP_ID_NULL). 
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MstStoreDlg.cpp  <br/> |CMsgStoreDlg::OnValidateIPMSubtree  <br/> |MFCMAPI использует **метод HrValidateIPMSubtree** для добавления стандартных папок в хранилище сообщений.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

