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
ms.openlocfilehash: 287577babc9a40b771aa9917211ba5dcbf8190ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584942"
---
# <a name="imapifolderemptyfolder"></a>IMAPIFolder::EmptyFolder

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Удаляет все сообщения и вложенные папки из папки без удаления самой папке.
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Дескриптор родительского окна индикатор хода выполнения. Параметр _ulUIParam_ игнорируется, пока флаг FOLDER_DIALOG будет выполнен с помощью параметра _ulFlags_ . 
    
 _lpProgress_
  
> [in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения. Если в _lpProgress_передается значение NULL, поставщика хранилища сообщений отображает индикатор выполнения с помощью реализация объекта MAPI хода выполнения. Параметр _lpProgress_ игнорируется, пока флаг FOLDER_DIALOG будет выполнен с помощью параметра _ulFlags_ . 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как папки. Можно задать следующие флажки:
    
DEL_ASSOCIATED 
  
> Удаляет все вложенные папки, включая вложенные папки, содержащие сообщения с связанный контент. Флаг DEL_ASSOCIATED имеет значение только для папки верхнего уровня, которое обрабатывает вызов.
    
DELETE_HARD_DELETE
  
> Безвозвратно удаляет все сообщения, включая удаленные из них.
    
FOLDER_DIALOG 
  
> Отображает индикатор хода выполнения во время операции.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Папка успешно очищается.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов завершился успешно, но папка не была полностью. При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Замечания

Метод **IMAPIFolder::EmptyFolder** удаляет все содержимое папки не удаляя саму папку. 
  
Во время вызова **EmptyFolder** отправляемого сообщения не удаляются. 
  
Связанное содержимое папки включают сообщения, которые используются для описания представлений, правил, настраиваемых форм и хранение пользовательских решений, а также может включать определения формы. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Не вызывайте метод [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) для сообщений в папке, которые были отправлены. Отправленные сообщения не удаляются. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Ожидается, что эти возвращаемые значения в следующих случаях.
  
|**Условие**|**������������ ��������**|
|:-----|:-----|
|**EmptyFolder** успешно очистки папки.  <br/> |ЗНАЧЕНИЕ S_OK  <br/> |
|**EmptyFolder** не удалось полностью очистить папку.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder** не удалось завершить.  <br/> |Любое значение ошибки  <br/> |
   
При **EmptyFolder** не удается завершить, не предполагают, что работа не выполнена. **EmptyFolder** мог на удаление папки перед ошибок. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnEmptyFolder  <br/> |Mfcmapi (en) использует метод **IMAPIFolder::EmptyFolder** для удаления содержимого указанной папки.  <br/> |
   
## <a name="see-also"></a>См. также



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Обработка ошибок с помощью макросов](using-macros-for-error-handling.md)

