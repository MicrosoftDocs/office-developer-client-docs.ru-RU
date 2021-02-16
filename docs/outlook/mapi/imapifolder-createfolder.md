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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает новую ветвь.
  
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
  
> [in] Тип создаемой папки. Можно установить следующие флаги:
    
FOLDER_GENERIC 
  
> Должна быть создана общая папка.
    
FOLDER_SEARCH 
  
> Необходимо создать папку результатов поиска.
    
 _lpszFolderName_
  
> [in] Указатель на строку, содержаную имя новой папки. Это имя является основой для свойства PR_DISPLAY_NAME **новой** папки ([PidTagDisplayName).](pidtagdisplayname-canonical-property.md)
    
 _lpszFolderComment_
  
> [in] Указатель на строку, которая содержит комментарий, связанный с новой папкой. Эта строка становится значением свойства PR_COMMENT **новой** папки ([PidTagComment).](pidtagcomment-canonical-property.md) Если передается NULL, у папки нет начального комментария.
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который будет использоваться для доступа к новой папке. Передача NULL приводит к возвращению поставщиком магазина сообщений стандартного интерфейса папки [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Клиенты должны передавать NULL. Другие вызыватели могут установить для  _параметра lpInterface_ IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer или IID_IMAPIFolder. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет процессом создания папки. Можно установить следующие флаги:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **CreateFolder** успешно возвращаться, возможно, до того, как новая папка будет полностью доступна вызываемому клиенту. Если новая папка недоступна, последующий вызов может привести к ошибке. 
    
MAPI_UNICODE 
  
> Имя папки имеет формат Юникод. Если флаг MAPI_UNICODE не установлен, имя папки будет в формате ANSI.
    
OPEN_IF_EXISTS 
  
> Позволяет успешно использовать метод, даже если папка с именем в параметре  _lpszFolderName_ уже существует, открыв существующую папку с таким именем. Обратите внимание, что поставщики store сообщений, которые позволяют папок одного и того же имени иметь одно и то же имя, могут не открывать существующую папку, если существует несколько папок с предоставленным именем. 
    
 _lppFolder_
  
> [out] Указатель на указатель на созданную папку.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Новая папка успешно создана или открыта, если OPEN_IF_EXISTS установлен.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.
    
MAPI_E_COLLISION 
  
> Папка с именем, заданным в  _параметре lpszFolderName,_ уже существует. Имена папок должны быть уникальными. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder::CreateFolder** создает вложенную папку в текущей папке и назначает идентификатор записи новой папке. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При **возвращении CreateFolder** следует помнить, что идентификатор записи для новой папки может быть не доступен. Некоторые поставщики store сообщений не делают идентификаторы записей доступными до тех пор, пока не будет вызван метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) новой папки для его постоянного сохранения. Это особенно актуально, если вы установили MAPI_DEFERRED_ERRORS флага. 
  
Следует помнить, что некоторые поставщики параметров хранения сообщений всегда указывают параметр _lppFolder_ на стандартный интерфейс папки независимо от значения параметра _lpInterface._ Так как возвращаемая указатель интерфейса может не иметь нужного типа, вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) новой папки, чтобы получить свойство **PR_OBJECT_TYPE** ([PidTagObjectType).](pidtagobjecttype-canonical-property.md) При необходимости перед другими вызовами приведите указатель к более подходящему типу.
  
Большинству поставщиков store сообщений требуется, чтобы имя новой папки было уникальным по отношению к именам ее папок одного и того же того же. Иметь возможность обрабатывать значение MAPI_E_COLLISION ошибки, которое возвращается, если это правило не следует. 
  
Чтобы определить идентификатор записи только что созданной папки, вызовите метод **IMAPIProp::GetProps** новой папки, чтобы получить ее свойство **PR_ENTRYID** ([PidTagEntryId).](pidtagentryid-canonical-property.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnCreateSubFolder  <br/> |MFCMAPI использует метод **CMsgStoreDlg::OnCreateSubFolder** для создания новых папок в MFCMAPI.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

