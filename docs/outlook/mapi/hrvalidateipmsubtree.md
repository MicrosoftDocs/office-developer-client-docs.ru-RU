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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Параметры

 _lpMDB_
  
> [in] Указатель на объект хранения сообщений, в который необходимо добавить папки. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, используемых для управления тем, как создаются папки. Можно установить следующие флаги:
    
MAPI_FORCE_CREATE 
  
> Папки должны быть проверены перед созданием, даже если свойства хранения сообщений указывают, что они действительны. Как правило, клиентские приложения устанавливают этот флаг, если ошибка указывает на то, что структура существующей папки повреждена. 
    
MAPI_FULL_IPM_TREE 
  
> Полный набор папок IPM должен быть создан в корневой папке хранения сообщений. В иерархии имеются такие заголовки папок:
    
    - Представления папок
    
    - Общие представления
    
    - Корень поиска\*
    
    - Подtree IPM\*
    
    - Inbox;
    
    - Исходящие
    
    - Удаленные элементы\*
    
    - Отправленные
    
    где три помеченные папки являются минимальным набором, созданным, даже если MAPI_FULL_IPM_TREE \* флага не установлен. Как правило, клиентские приложения устанавливают этот флаг, если хранилище сообщений, в котором будут созданы папки, является хранилищем по умолчанию.
    
 _lpcValues_
  
> [in, out] Указатель на число структур [SPropValue](spropvalue.md) в массиве, возвращаемом в _параметре lppProps._ Значение параметра  _lpcValues_ может быть нулем, если  _lppProps_ имеет значение NULL. 
    
 _lppProps_
  
> [in, out] Указатель на указатель на массив структур **SPropValue,** содержащий значения свойств для **свойства PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask)](pidtagvalidfoldermask-canonical-property.md)и для соответствующих свойств идентификатора записи папки. Если **HrValidateIPMSubtree** создает в хранилище сообщений почтовый ящик, массив **SPropValue** включает идентификатор записи "Входящие" со специальным тегом свойства, закодированные как  `PROP_TAG(PT_BINARY, PROP_ID_NULL)` . Параметр _lppProps_ может иметь параметр NULL, указывающий, что для реализации вызова не требуется возвращать массив **SPropValue.** 
    
 _lppMapiError_
  
> [out] Указатель на указатель на структуру [MAPIERROR,](mapierror.md) которая содержит сведения о версии, компоненте и контексте для ошибки. Если структура **MAPIERROR** не возвращается, для параметра _lppMAPIError_ задано NULL. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

MAPI использует функцию **HrValidateIPMSubtree** внутри компании для создания стандартного поддерева IPM в хранилище сообщений при первом открытие магазина или при его встраии в хранилище по умолчанию. Эта функция также может использоваться клиентских приложений для проверки или восстановления стандартных папок сообщений. 
  
 **HrValidateIPMSubtree** всегда создает папки "Корень поиска" и "Поддерево IPM" в корневой папке магазина, а папка "Удаленные" в папке поддерева IPM. Папка поддерево IPM является корневым корнем иерархии IPM в этом хранилище сообщений. Корневую папку поиска можно использовать в качестве корня поддерево для папок результатов поиска. 
  
Клиенты IPM должны отображать представление папки, начиная с корневой папки поддеревого IPM и отображая под ней свои папки. Сведения в корневой папке хранения сообщений не должны отображаться в пользовательском интерфейсе клиента. Эта функция означает, что если клиенту необходимо скрыть сведения, эти сведения можно поместить в корневой каталог подстановки IPM, где они не видны пользователю. С другой стороны, приложения, не вложенные в IPM, которые требуют, чтобы сообщения и папки были невидимыми для пользователя, например в серверном хранилище сообщений, могут поместить их за пределы иерархии IPM. 
  
 **HrValidateIPMSubtree** задает свойство **PR_VALID_FOLDER_MASK,** чтобы указать, имеет ли каждая создаемая папка IPM допустимый идентификатор записи. Следующие свойства идентификатора записи в хранилище сообщений заданы для идентификаторов записей соответствующих папок и возвращаются в _параметре lppProps_ вместе с **PR_VALID_FOLDER_MASK:** 
  
 **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId)](pidtagcommonviewsentryid-canonical-property.md)
  
> **PR_FINDER_ENTRYID** ([PidTagFinderEntryId)](pidtagfinderentryid-canonical-property.md)
  
> **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId)](pidtagipmoutboxentryid-canonical-property.md)
  
> **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId)](pidtagipmsentmailentryid-canonical-property.md)
  
> **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId)](pidtagipmsubtreeentryid-canonical-property.md)
  
> **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId)](pidtagipmwastebasketentryid-canonical-property.md)
  
> **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId)](pidtagviewsentryid-canonical-property.md)
  
> Замещего [PROP_TAG](prop_tag.md) для почтового ящика IPM (PT_BINARY, PROP_ID_NULL). 
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MstStoreDlg.cpp  <br/> |CMsgStoreDlg::OnValidateIPMSubtree  <br/> |MFCMAPI использует метод **HrValidateIPMSubtree** для добавления стандартных папок в хранилище сообщений.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

