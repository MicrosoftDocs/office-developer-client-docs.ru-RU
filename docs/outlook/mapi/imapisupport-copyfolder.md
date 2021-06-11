---
title: IMAPISupportCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyFolder
api_type:
- COM
ms.assetid: c2e0939f-0668-473f-856c-a27af094070b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 11ee944a14f8c9bd881b9c79a4ce66817275e73a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420887"
---
# <a name="imapisupportcopyfolder"></a>IMAPISupport::CopyFolder

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Копирует или перемещает папку из текущей родительской папки в другую родительную.
  
```cpp
HRESULT CopyFolder(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  LPSTR lpszNewFolderName,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpSrcInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к родительской папке папки, которая будет скопирована или перемещена.
    
 _lpSrcFolder_
  
> [in] Указатель на родительную папку папки, которая будет скопирована или перемещена. 
    
 _cbEntryID_
  
> [in] Byte count in the entry identifier pointed to by _lpEntryID._
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи папки, которая будет скопирована или перемещена. 
    
 _lpInterface_
  
> [in] Зарезервировано; должно быть NULL.
    
 _lpDestFolder_
  
> [in] Указатель на папку, которая должна быть скопирована или перемещена.
    
 _lpszNewFolderName_
  
> [in] Указатель на имя скопированной или перемещенной папки; в противном случае NULL, которая указывает, что скопированная или перемещенная папка должна иметь то же имя, что и исходные папки (папка, на которую указывает _lpEntryID)._
    
 _ulUIParam_
  
> [in] Ручка окна для диалогового окна индикатора прогресса и связанных окон. Параметр _ulUIParam_ игнорируется, если флаг FOLDER_DIALOG в параметре _ulFlags._ 
    
 _lpProgress_
  
> [in] Указатель на объект progress, отображает индикатор прогресса. Если NULL передается в  _lpProgress,_ поставщик магазина сообщений отображает индикатор прогресса с помощью реализации объекта progress MAPI. Параметр  _lpProgress_ игнорируется, если флаг FOLDER_DIALOG не установлен в  _ulFlags_.
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют выполнение операции копирования или перемещения. Можно установить следующие флаги:
    
COPY_SUBFOLDERS 
  
> Все подмостки папки должны быть скопированы или перемещены. Если COPY_SUBFOLDERS не задан для операции копирования, копируется только папка, идентифицированная _lpEntryID._ При операции перемещения поведение COPY_SUBFOLDERS по умолчанию независимо от того, установлен ли флаг. 
    
FOLDER_DIALOG 
  
> Запрашивает отображение индикатора прогресса.
    
FOLDER_MOVE 
  
> Папка должна быть перемещена, а не скопирована. Если FOLDER_MOVE не установлено, папка копируется.
    
MAPI_UNICODE 
  
> Имя папки находится в формате Unicode. Если флаг MAPI_UNICODE не установлен, имя папки находится в формате ANSI.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Папка успешно скопирована или перемещена.
    
MAPI_E_COLLISION 
  
> Имя перемещаемой или копируется папки так же, как и имя подмостка в папке назначения. Поставщик магазина сообщений требует, чтобы имена папок были уникальными. Операция прекращается без завершения.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов удался, но не все записи были успешно скопированы. Когда это предупреждение возвращается, вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Для объектов поддержки поставщика сообщений реализован метод **IMAPISupport::CopyFolder.** Поставщики магазинов сообщений могут вызывать **IMAPISupport::CopyFolder** при реализации [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) для копирования или перемещения одной папки из одной родительской папки в другую. 
  
 **IMAPISupport::CopyFolder** добавляет скопированную или перемещенную папку в подмостки папки назначения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **IMAPISupport::CopyFolder** позволяет одновременное переименование и перемещение папок, а также копирование или перемещение подмостков затрагиваемой папки. Чтобы скопировать или переместить все подмостки, вложенные в скопированную или перемещенную папку, передай флаг COPY_SUBFOLDERS в  _ulFlags_. 
  
Ожидайте следующие значения возврата при следующих условиях:
  
|**Condition**|**Возвращаемое значение**|
|:-----|:-----|
|**CopyFolder** успешно скопировал или переместил папку и все ее подмостки, если это применимо.  <br/> |S_OK  <br/> |
|**CopyFolder** не удалось успешно скопировать или переместить все папки.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder** не удалось выполнить.  <br/> |Любое значение ошибки  <br/> |
   
Если **CopyFolder** возвращает значение ошибки, не делайте предположение, что не было сделано никакой работы. Одна или несколько папок могли быть скопированы или перемещены до сбоя **CopyFolder.** 
  
## <a name="see-also"></a>См. также



[IMAPISupport: IUnknown](imapisupportiunknown.md)

