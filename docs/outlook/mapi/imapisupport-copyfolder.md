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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Копирует или перемещает папку из текущей родительской папки в другую родительную папку.
  
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

## <a name="parameters"></a>Параметры

 _lpSrcInterface_
  
> [in] Указатель на идентификатор интерфейса , который представляет интерфейс, используемый для доступа к родительской папке папки для копирования или перемещений.
    
 _lpSrcFolder_
  
> [in] Указатель на родительская папка папки, которая должна быть скопирована или перемещена. 
    
 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает _lpEntryID._
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи папки, которая должна быть скопирована или перемещена. 
    
 _lpInterface_
  
> [in] Зарезервировано; должно быть NULL.
    
 _lpDestFolder_
  
> [in] Указатель на папку, которая должна быть скопирована или перемещена.
    
 _lpszNewFolderName_
  
> [in] Указатель на имя скопированной или перемещенной папки; в противном случае NULL указывает, что скопированная или перемещенная папка должна иметь то же имя, что и у папки источника (папка, на которую указывает _lpEntryID)._
    
 _ulUIParam_
  
> [in] Handle of the window for the progress indicator dialog box and related windows. Параметр  _ulUIParam_ игнорируется, если FOLDER_DIALOG в параметре  _ulFlags_ не задан флаг FOLDER_DIALOG. 
    
 _lpProgress_
  
> [in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения. Если в  _lpProgress_ передается NULL, поставщик хранилище сообщений отображает индикатор хода выполнения с помощью реализации объекта хода выполнения MAPI. Параметр _lpProgress_ игнорируется, если флаг FOLDER_DIALOG не установлен в _ulFlags._
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет выполнением операции копирования или перемещения. Можно установить следующие флаги:
    
COPY_SUBFOLDERS 
  
> Все вложенные папки папки должны быть скопированы или перемещены. Если COPY_SUBFOLDERS не задан для операции копирования, копируется только папка, заданная _lpEntryID._ При операции перемещения поведение COPY_SUBFOLDERS по умолчанию независимо от того, установлен ли флаг. 
    
FOLDER_DIALOG 
  
> Запрашивает отображение индикатора хода выполнения.
    
FOLDER_MOVE 
  
> Папка должна быть перемещена вместо копирования. Если FOLDER_MOVE не установлен, папка копируется.
    
MAPI_UNICODE 
  
> Имя папки имеет формат Юникод. Если флаг MAPI_UNICODE не установлен, имя папки будет в формате ANSI.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Папка успешно скопирована или перемещена.
    
MAPI_E_COLLISION 
  
> Имя перемещаемой или копируется папки так же, как и имя вложенной папки в конечной папке. Поставщику store сообщений требуется, чтобы имена папок были уникальными. Операция останавливается без завершения.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов был успешным, но не все записи были успешно скопированы. При возвращении этого предупреждения вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **макрос HR_FAILED.** Дополнительные сведения см. в [теме "Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::CopyFolder** реализован для объектов поддержки поставщика хранения сообщений. Поставщики store сообщений могут вызывать **IMAPISupport::CopyFolder** в своей реализации [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) для копирования или перемещения одной папки из одной родительской папки в другую. 
  
 **IMAPISupport::CopyFolder** добавляет скопированную или перемещенную папку в качестве вложенной папки назначения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **IMAPISupport::CopyFolder** позволяет одновременно переименовывание и перемещение папок, а также копирование или перемещение вложенных папок затронутой папки. Чтобы скопировать или переместить все вложенные папки, вложенные в скопированную или перемещенную папку, передав флаг COPY_SUBFOLDERS в _ulFlags._ 
  
При следующих условиях следует ожидать следующих возвращаемых значений:
  
|**Condition**|**Возвращаемое значение**|
|:-----|:-----|
|**CopyFolder** успешно скопировал или переместил папку и все ее вложенные папки, если это применимо.  <br/> |S_OK  <br/> |
|**CopyFolder** не удалось успешно скопировать или переместить все папки.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder** не удалось завершить.  <br/> |Любое значение ошибки  <br/> |
   
Если **CopyFolder** возвращает значение ошибки, не переходите к предположению о том, что работа не была сделана. Одна или несколько папок могли быть скопированы или перемещены до того, как **в CopyFolder** сбой. 
  
## <a name="see-also"></a>См. также



[IMAPISupport: IUnknown](imapisupportiunknown.md)

