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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Удаляет все сообщения и вложенные папки из папки без удаления самой папки.
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Handle to the parent window of the progress indicator. Параметр  _ulUIParam_ игнорируется, если FOLDER_DIALOG в параметре  _ulFlags_ не задан флаг FOLDER_DIALOG. 
    
 _lpProgress_
  
> [in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения. Если в  _lpProgress_ передается NULL, поставщик хранилище сообщений отображает индикатор хода выполнения с помощью реализации объекта хода выполнения MAPI. Параметр _lpProgress_ игнорируется, если FOLDER_DIALOG флага в параметре _ulFlags._ 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет опустошаемой папкой. Можно установить следующие флаги:
    
DEL_ASSOCIATED 
  
> Удаляет все ведерки, в том числе вудерки, содержащие сообщения со связанным содержимым. Флаг DEL_ASSOCIATED имеет значение только для папки верхнего уровня, с чем действует вызов.
    
DELETE_HARD_DELETE
  
> Окончательно удаляет все сообщения, включая сообщения, удаленные с удалением.
    
FOLDER_DIALOG 
  
> Отображает индикатор хода выполнения операции.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Папка успешно очищена.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов был успешным, но папка не была полностью очищена. При возвращении этого предупреждения вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **макрос** HR_FAILED. Дополнительные сведения см. в [теме "Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder::EmptyFolder** удаляет все содержимое папки без удаления самой папки. 
  
Во время **вызова EmptyFolder** отправленные сообщения не удаляются. 
  
Связанное с папкой содержимое содержит сообщения, которые используются для описания представлений, правил, настраиваемые формы и хранилища пользовательских решений, а также могут включать определения форм. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Не вызываем метод [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) для сообщений в папке, которые были отправлены. Отправленные сообщения не удаляются. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Эти возвращаемые значения следует ожидать при следующих условиях.
  
|**Condition**|**Возвращаемое значение**|
|:-----|:-----|
|**EmptyFolder** успешно опустошил папку.  <br/> |S_OK  <br/> |
|**EmptyFolder** не удалось полностью очистить папку.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder** не удалось завершить.  <br/> |Любое значение ошибки  <br/> |
   
Если **EmptyFolder** не может завершиться, не предполагать, что никаких трудоемких работ не было. **EmptyFolder** мог удалить часть содержимого папки до того, как произошла ошибка. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnEmptyFolder  <br/> |MFCMAPI использует метод **IMAPIFolder::EmptyFolder** для удаления содержимого указанной папки.  <br/> |
   
## <a name="see-also"></a>См. также



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Использование макроса для обработки ошибок](using-macros-for-error-handling.md)

