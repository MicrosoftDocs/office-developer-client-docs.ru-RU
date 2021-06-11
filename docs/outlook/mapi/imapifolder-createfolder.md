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
ms.openlocfilehash: 606d780aa59e363c30ddc7a5b562db64d845ccb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436764"
---
# <a name="imapifoldercreatefolder"></a>IMAPIFolder::CreateFolder

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает новый подмосток.
  
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

## <a name="parameters"></a>Parameters

 _ulFolderType_
  
> [in] Тип папки для создания. Можно установить следующие флаги:
    
FOLDER_GENERIC 
  
> Должна быть создана общая папка.
    
FOLDER_SEARCH 
  
> Необходимо создать папку результатов поиска.
    
 _lpszFolderName_
  
> [in] Указатель на строку, содержаную имя новой папки. Это имя является основой для свойства  PR_DISPLAY_NAME[(PidTagDisplayName).](pidtagdisplayname-canonical-property.md)
    
 _lpszFolderComment_
  
> [in] Указатель на строку, содержаную комментарий, связанный с новой папкой. Эта строка становится значением свойства  PR_COMMENT[(PidTagComment).](pidtagcomment-canonical-property.md) Если NULL передается, у папки нет начального комментария.
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к новой папке. Передача NULL заставляет поставщика хранения сообщений возвращать стандартный интерфейс папки [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Клиенты должны пройти NULL. Другие звонители могут установить параметр  _lpInterface_ для IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer или IID_IMAPIFolder. 
    
 _ulFlags_
  
> [in] Битмаска флагов, контролируемая тем, как создается папка. Можно установить следующие флаги:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **CreateFolder** успешно возвращаться, возможно, до того, как новая папка будет полностью доступна для вызываемого клиента. Если новая папка недоступна, последующий вызов может привести к ошибке. 
    
MAPI_UNICODE 
  
> Имя папки находится в формате Unicode. Если флаг MAPI_UNICODE не установлен, имя папки находится в формате ANSI.
    
OPEN_IF_EXISTS 
  
> Позволяет методу добиться успеха, даже если папка, названная в параметре  _lpszFolderName,_ уже существует, открыв существующую папку с таким именем. Обратите внимание, что поставщики магазинов сообщений, которые позволяют папкам-однобрачам иметь одно имя, могут не открывать существующую папку, если с предоставленным именем существует несколько. 
    
 _lppFolder_
  
> [вышел] Указатель на указатель на вновь созданную папку.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Новая папка успешно создана или открыта, если OPEN_IF_EXISTS установлен флаг.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.
    
MAPI_E_COLLISION 
  
> Папка с именем, заданным в  _параметре lpszFolderName,_ уже существует. Имена папок должны быть уникальными. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder::CreateFolder** создает подмостки в текущей папке и назначает идентификатор входа в новую папку. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Когда **CreateFolder** возвращается, следует помнить, что идентификатор записи для новой папки может быть недоступным. Некоторые поставщики магазинов сообщений не делают идентификаторы записей доступными до тех пор, пока не будет вызван метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) новой папки для его постоянного сохранения. Это особенно актуально, если вы установили флаг MAPI_DEFERRED_ERRORS. 
  
Следует помнить, что некоторые поставщики магазинов сообщений всегда указывают параметр _lppFolder_ на стандартный интерфейс папки, независимо от значения, которое вы передаете для _параметра lpInterface._ Поскольку возвращаемая указатель интерфейса может быть не того типа, который вы ожидаете, позвоните по методу [IMAPIProp::GetProps](imapiprop-getprops.md) новой **папки,** чтобы получить свойство [PR_OBJECT_TYPE (PidTagObjectType).](pidtagobjecttype-canonical-property.md) При необходимости переведите указатель в более подходящий тип перед другими вызовами.
  
Большинство поставщиков магазинов сообщений требуют, чтобы имя новой папки было уникальным по отношению к именам его папок-окантов. Возможность обработки значения MAPI_E_COLLISION ошибки, которое возвращается, если это правило не следует. 
  
Чтобы определить идентификатор записи вновь созданной папки, позвоните по методу **IMAPIProp::GetProps** новой папки, чтобы получить ее свойство [PR_ENTRYID (PidTagEntryId).](pidtagentryid-canonical-property.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnCreateSubFolder  <br/> |MFCMAPI использует **метод CMsgStoreDlg::OnCreateSubFolder** для создания новых папок в MFCMAPI.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

