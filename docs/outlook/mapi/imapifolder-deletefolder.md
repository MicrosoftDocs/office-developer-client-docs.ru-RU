---
title: IMAPIFolderDeleteFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteFolder
api_type:
- COM
ms.assetid: 6c3e883c-80c0-4eda-8f81-8277d933a74b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a476607927f3563ede94a04ccfe4f7a3749c978e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417408"
---
# <a name="imapifolderdeletefolder"></a>IMAPIFolder::DeleteFolder

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Удаляет в подсайт.
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи в подкамере, который необходимо удалить.
    
 _ulUIParam_
  
> [in] Handle to the parent window of the progress indicator. Параметр  _ulUIParam_ игнорируется, если FOLDER_DIALOG в параметре  _ulFlags_ не задан флаг FOLDER_DIALOG. 
    
 _lpProgress_
  
> [in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения. Если в  _lpProgress_ передается NULL, поставщик хранилище сообщений отображает индикатор хода выполнения с помощью реализации объекта хода выполнения MAPI. Параметр _lpProgress_ игнорируется, если флаг FOLDER_DIALOG не установлен в _ulFlags._
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет удалением вуза. Можно установить следующие флаги:
    
DEL_FOLDERS 
  
> Все впапные в подпапки, на которые указывает  _lpEntryID,_ необходимо удалить. 
    
DEL_MESSAGES 
  
> Все сообщения в подпапке, на которые указывает  _lpEntryID,_ должны быть удалены. 
    
FOLDER_DIALOG 
  
> Индикатор хода выполнения должен отображаться во время выполнения операции.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Указанная папка успешно удалена.
    
MAPI_E_HAS_FOLDERS 
  
> В удаляемой в подкамере содержатся в том же DEL_FOLDERS, что и флаг DEL_FOLDERS не установлен. В подмайки не были удалены.
    
MAPI_E_HAS_MESSAGES 
  
> В удаляемой подкамере содержатся сообщения, флаг DEL_MESSAGES не установлен. Подкамерка не была удалена.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов был успешным, но не все записи были успешно удалены. При возвращении этого предупреждения вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **макрос HR_FAILED.** Дополнительные сведения см. в [теме "Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder::D eleteFolder** удаляет впапную. По умолчанию **DeleteFolder** работает только с пустыми папками, но его можно успешно использовать для непустых папок, установив два флага: DEL_FOLDERS и DEL_MESSAGES. Удалять можно только пустые папки или папки, DEL_FOLDERS и DEL_MESSAGES флаги для вызова **DeleteFolder.** DEL_FOLDERS позволяет удалить все вложенные папки папки; DEL_MESSAGES позволяет удалять все сообщения папки. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если операция удаления включает несколько папок, выполните ее как можно точнее для каждой папки. Иногда одна из удаляемой папки не существует или была перемещена или скопирована в другое место. Не останавливайте операцию раньше времени, если не произойдет сбой, который находится вне вашего контроля, например, если недостаточно памяти, недостаточно места на диске или не будет повреждения в хранилище сообщений.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Эти возвращаемые значения следует ожидать при следующих условиях.
  
|**Condition**|**Возвращаемое значение**|
|:-----|:-----|
|**DeleteFolder** успешно удалил все сообщения и в подкамеру.  <br/> |S_OK  <br/> |
|**DeleteFolder** не удалось успешно удалить все сообщения и в подкамеру.  <br/> |MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND  <br/> |
|**DeleteFolder** не удалось завершить.  <br/> |Любое значение ошибки, кроме MAPI_E_NOT_FOUND  <br/> |
   
Если **deleteFolder** не удается завершить, не предполагайте, что никаких работ не было сделано. **Возможно, deleteFolder** удалось удалить одно или несколько сообщений и вудерок, прежде чем столкнуться с ошибкой. 
  
Если не удается удалить одну или несколько ветвей, **DeleteFolder** возвращает MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND в зависимости от реализации поставщика store сообщений. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDeleteSelectedItem  <br/> |MFCMAPI использует метод **IMAPIFolder::D eleteFolder** для удаления папок.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

