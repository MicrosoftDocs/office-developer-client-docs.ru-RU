---
title: IMAPIFolderCreateFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateFolder
api_type:
- COM
ms.assetid: 39d07fc8-09aa-4122-af32-b02f2c893d29
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 694f7ec5715a7348c9bd90c28d14f30d43d19974
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581785"
---
# <a name="imapifoldercreatefolder"></a>IMAPIFolder::CreateFolder

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает папку.
  
```cpp
HRESULT CreateFolder(
  ULONG ulFolderType,
  LPSTR lpszFolderName,
  LPSTR lpszFolderComment,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMAPIFOLDER FAR * lppFolder
);
```

## <a name="parameters"></a>Параметры

 _ulFolderType_
  
> [in] Тип папки для создания. Можно задать следующие флажки:
    
FOLDER_GENERIC 
  
> Должен быть создан общей папки.
    
FOLDER_SEARCH 
  
> Должен быть создан в папку результатов поиска.
    
 _lpszFolderName_
  
> [in] Указатель на строку, содержащую имя новой папки. Это имя является основой для свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) новую папку.
    
 _lpszFolderComment_
  
> [in] Указатель на строку, которая содержит комментарий, связанный с новой папки. Эта строка становится значением свойства **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) новую папку. Если передается значение NULL, папка содержит начальной комментарий.
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к новой папки. Значение NULL вызывает поставщика хранилища сообщений для возврата интерфейсе стандартные папки [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Клиенты необходимо передать значение NULL. Другие абонентов можно включить параметр _lpInterface_ IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer или IID_IMAPIFolder. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как создать папку. Можно задать следующие флажки:
    
MAPI_DEFERRED_ERRORS 
  
> Разрешает **CreateFolder** для возврата успешно, возможно перед новой папки доступными для клиента. Если новую папку не поддерживается, последующие подключения к нему может вызвать ошибку. 
    
MAPI_UNICODE 
  
> — Это имя папки в формате Юникод. Если флаг MAPI_UNICODE не установлен, — это имя папки в формате ANSI.
    
OPEN_IF_EXISTS 
  
> Позволяет методу успешной даже в том случае, если папку с именем в параметре _lpszFolderName_ уже существует, откройте существующую папку с таким именем. Обратите внимание на то, что поставщиков хранилища сообщений, которые позволяют одноуровневого папок, с одинаковыми именами не может открыть существующую папку, если существует несколько экземпляров с заданным именем. 
    
 _lppFolder_
  
> [out] Указатель на указатель на только что созданная папка.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Новую папку были успешно создана или открыта, если флаг OPEN_IF_EXISTS установлен.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.
    
MAPI_E_COLLISION 
  
> Папка, которая имеет имя, присвоенное с помощью параметра _lpszFolderName_ уже существует. Имена папок должно быть уникальным. 
    
## <a name="remarks"></a>Замечания

Метод **IMAPIFolder::CreateFolder** создает вложенную папку в текущей папке и назначает идентификатор записи в новую папку. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При возврате **CreateFolder** , обратите внимание, что идентификатор записи на новую папку может быть недоступна. Некоторые поставщики хранения сообщения не предоставляют идентификаторы записей до после вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) новую папку для сохранения ее без возможности восстановления. Это особенно важно, если выбрать флаг MAPI_DEFERRED_ERRORS. 
  
Обратите внимание, что некоторые поставщики хранилища сообщений всегда указывать параметр _lppFolder_ стандартный интерфейс папки, независимо от того, значение, переданное для параметра _lpInterface_ . Указатель интерфейса, который возвращается может быть типа, предполагается, что, вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) новую папку для получения свойства **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)). При необходимости привести указатель на более подходящий тип, прежде чем принять других вызовов.
  
Большинство поставщиков хранилища сообщений требуется имя новой папки должно быть уникальным по отношению к имена его папки. Иметь возможность обрабатывать MAPI_E_COLLISION об ошибке, которое возвращается, если это правило не следует. 
  
Чтобы определить идентификатор записи только что созданная папка, вызовите метод **IMAPIProp::GetProps** новую папку для получения его свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnCreateSubFolder  <br/> |Mfcmapi (en) использует метод **CMsgStoreDlg::OnCreateSubFolder** для создания новой папки в mfcmapi (en).  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

