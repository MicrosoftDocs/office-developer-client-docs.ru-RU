---
title: IMAPIFolderEmptyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.EmptyFolder
api_type:
- COM
ms.assetid: 4cfcb498-9182-4906-bd6f-d9bc387bc88b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4ca828c3e03cbff886230f2af63485f7b15e8b35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416785"
---
# <a name="imapifolderemptyfolder"></a>IMAPIFolder::EmptyFolder

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет все сообщения и подмостки из папки без удаления самой папки.
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Ручка родительского окна индикатора прогресса. Параметр _ulUIParam_ игнорируется, если флаг FOLDER_DIALOG в параметре _ulFlags._ 
    
 _lpProgress_
  
> [in] Указатель на объект progress, отображает индикатор прогресса. Если NULL передается в  _lpProgress,_ поставщик магазина сообщений отображает индикатор прогресса с помощью реализации объекта progress MAPI. Параметр _lpProgress_ игнорируется, если флаг FOLDER_DIALOG в параметре _ulFlags._ 
    
 _ulFlags_
  
> [in] Битмашка флагов, контролирующих, как очищается папка. Можно установить следующие флаги:
    
DEL_ASSOCIATED 
  
> Удаляет все подмостки, включая подмостки, содержащие сообщения со связанным содержимым. Флаг DEL_ASSOCIATED имеет значение только для папки верхнего уровня, на которая действует вызов.
    
DELETE_HARD_DELETE
  
> Постоянно удаляет все сообщения, в том числе удаленные с мягкими сообщениями.
    
FOLDER_DIALOG 
  
> Отображает индикатор прогресса во время выполнения операции.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Папка успешно опустошалась.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов удался, но папка не была полностью очищена. Когда это предупреждение возвращается, вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder::EmptyFolder** удаляет все содержимое папки без удаления самой папки. 
  
Во время **вызова EmptyFolder** отправленные сообщения не удаляются. 
  
Связанное содержимое папки включает сообщения, которые используются для описания представлений, правил, настраиваемой формы и хранения настраиваемого решения, а также могут включать определения форм. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Не вызывай [метод IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) для сообщений в отправленной папке. Отправленные сообщения не удаляются. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Ожидайте этих значений возврата в следующих условиях.
  
|**Condition**|**Возвращаемое значение**|
|:-----|:-----|
|**EmptyFolder** успешно опорожняет папку.  <br/> |S_OK  <br/> |
|**EmptyFolder** не смог полностью очистить папку.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder** не удалось выполнить.  <br/> |Любое значение ошибки  <br/> |
   
Если **EmptyFolder** не удается выполнить, не думайте, что работа не была сделана. **EmptyFolder,** возможно, удалось удалить часть содержимого папки, прежде чем столкнуться с ошибкой. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnEmptyFolder  <br/> |MFCMAPI использует **метод IMAPIFolder::EmptyFolder** для удаления содержимого указанной папки.  <br/> |
   
## <a name="see-also"></a>См. также



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Использование макроса для обработки ошибок](using-macros-for-error-handling.md)

