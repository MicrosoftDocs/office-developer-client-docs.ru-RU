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
ms.openlocfilehash: 2625b148d15c2f5ccf65eedf3a1b1f2c9d0d133e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592047"
---
# <a name="hrvalidateipmsubtree"></a>HrValidateIPMSubtree

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Добавление папки электронной почты — это стандартные сообщений (IPM) хранилища сообщений. 
  
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
  
> [in] Указатель на сообщение хранения объектов, в которую нужно добавить в папки. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, используемые для управления Создание папки. Можно задать следующие флажки:
    
MAPI_FORCE_CREATE 
  
> Папки следует проверить перед созданием, даже в том случае, если свойства хранилища сообщений показывают, что они являются допустимыми. Клиентское приложение обычно устанавливает этот флаг при появится сообщение о том поврежден структура существующую папку. 
    
MAPI_FULL_IPM_TREE 
  
> Полный набор папок IPM должны создаваться в корневую папку хранилища сообщений. Названия папок в иерархии являются:
    
    - Представления папок
    
    - Общие представления
    
    - Корневая папка поиска\*
    
    - Поддерева IPM\*
    
    - Inbox
    
    - Исходящие
    
    - "Удаленные"\*
    
    - Отправленные элементы
    
    где отмеченный три папки \* являются минимальный набор создан даже в том случае, если флаг MAPI_FULL_IPM_TREE не задано. Клиентское приложение обычно устанавливает этот флаг при хранилища сообщений, в котором будут создаваться папки — это хранилище по умолчанию.
    
 _lpcValues_
  
> [in, out] Указатель на число структур [SPropValue](spropvalue.md) в массива, возвращаемого в параметре _lppProps_ . Значение параметра _lpcValues_ может быть равно нулю, если _lppProps_ имеет значение NULL. 
    
 _lppProps_
  
> [in, out] Указатель на указатель для массива структур **SPropValue** , который содержит значения свойств для свойства **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)), а также для свойства идентификатор записи соответствующую папку. Если **HrValidateIPMSubtree** создает папки "Входящие" в хранилище сообщений, массива **SPropValue** включает в себя идентификатор записи папки "Входящие" с тег специальные свойства, кодированных как `PROP_TAG(PT_BINARY, PROP_ID_NULL)`. Параметр _lppProps_ может быть NULL, указывающего на то, что вызывающий реализации не требуется, что возвращаться массив **SPropValue** . 
    
 _lppMapiError_
  
> [out] Указатель на указатель на структуру [MAPIERROR](mapierror.md) , который содержит сведения о версии, компонент и контекста для ошибки. Параметр _lppMAPIError_ задано значение NULL, если структура не **MAPIERROR** возвращается. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

MAPI функция **HrValidateIPMSubtree** во внутренней сети для создания стандартных поддерева IPM в хранилище сообщений при первом открытии хранилища или хранилища выполняется хранения по умолчанию. Также эта функция можно использовать с клиентскими приложениями для проверки или исправления папки стандартных сообщений. 
  
 **HrValidateIPMSubtree** всегда создает папки поиска корневые папки и поддерева IPM в хранилище корневой папки и папки «Удаленные» в папке поддерева IPM. Папка поддерева IPM — корневой каталог иерархии IPM в этого хранилища сообщений. Поиск корневую папку можно использовать в качестве корневого поддерева для результатов поиска папок. 
  
Клиенты IPM должны отображать их представления папок, начиная с корневой папки поддерева IPM и отображение дочерних папок под ним. Сведения в корневую папку хранилища сообщений не должно быть в пользовательский интерфейс клиента. Данная функциональная возможность означает, что если это клиент должен скрывать сведения, сведения может быть помещена в корневом каталоге поддерева IPM которых не отображается для пользователя. С другой стороны не являющиеся IPM приложений, которым требуется сообщений и папок быть невидимым для пользователя, например в хранилище сообщений на стороне сервера, их можно поместить за пределами иерархии IPM. 
  
 **HrValidateIPMSubtree** задает свойство **PR_VALID_FOLDER_MASK** значение, указывающее, является ли каждой папки IPM, которые он создает допустимым идентификатором. Следующие свойства идентификатор записи хранилища сообщений задать идентификаторы записей из соответствующих папок и возвращаются в параметре _lppProps_ , а также **PR_VALID_FOLDER_MASK**: 
  
 **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))
  
> **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))
  
> **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
  
> **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
  
> **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
  
> **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
  
> **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))
  
> Заполнитель [PROP_TAG](prop_tag.md) для IPM папки «Входящие» (PT_BINARY, PROP_ID_NULL). 
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MstStoreDlg.cpp  <br/> |CMsgStoreDlg::OnValidateIPMSubtree  <br/> |Mfcmapi (en) метод **HrValidateIPMSubtree** используется для добавления стандартные папки для хранения сообщений.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

