---
title: IMAPIFolderDeleteMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteMessages
api_type:
- COM
ms.assetid: 5a16e62b-9d33-41cd-af2b-9abd403b6f2e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bd0439c71df7083e3c4787a5d317fa11d2b99c61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578635"
---
# <a name="imapifolderdeletemessages"></a>IMAPIFolder::DeleteMessages

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Удаляет одно или несколько сообщений.
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpMsgList_
  
> [in] Указатель на структуру [ENTRYLIST](entrylist.md) , содержащее число сообщений для удаления и массив структур [ENTRYID](entryid.md) , чтобы указать сообщения. 
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна индикатор хода выполнения. Параметр _ulUIParam_ игнорируется, пока флаг MESSAGE_DIALOG будет выполнен с помощью параметра _ulFlags_ . 
    
 _lpProgress_
  
> [in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения. Если в _lpProgress_передается значение NULL, поставщика хранилища сообщений отображает индикатор выполнения с помощью реализация объекта MAPI хода выполнения. Параметр _lpProgress_ игнорируется, пока флаг MESSAGE_DIALOG будет выполнен с помощью параметра _ulFlags_ . 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как сообщения будут удалены. Можно задать следующие флажки:
    
DELETE_HARD_DELETE
  
> Безвозвратно удаляет все сообщения, включая удаленные из них.
    
MESSAGE_DIALOG 
  
> Отображает индикатор выполнения, как операция продолжается.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Указанный сообщения или сообщения были успешно удалены.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов завершился успешно, но не все сообщения были успешно удалены. При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Замечания

Метод **IMAPIFolder::DeleteMessages** удаляет сообщения из папки. Не удается удалить сообщения, не существует, были перемещены в другом месте, открытые с разрешением на чтение и запись или, представленных в настоящее время. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

При операции удаления состоит из нескольких сообщений, выполните операцию, как можно для каждой папки даже в том случае, если не удается удалить один или несколько сообщений. Не останавливайте операции преждевременно Если произошла ошибка, которая находится за пределами элементу управления, такие как хватает памяти, недостаточно места на диске или повреждение в хранилище сообщений.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Ожидается, что эти возвращаемые значения в следующих случаях.
  
|**Условие**|**������������ ��������**|
|:-----|:-----|
|**DeleteMessages** успешно удален каждого сообщения.  <br/> |ЗНАЧЕНИЕ S_OK  <br/> |
|**DeleteMessages** не удалось успешно удалить все сообщения и вложенной папке.  <br/> |MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages** не удалось завершить.  <br/> |Любое значение ошибки, за исключением MAPI_E_NOT_FOUND  <br/> |
   
При **DeleteMessages** не удается завершить, не предполагают, что работа не выполнена. **DeleteMessages** мог удалить одно или несколько сообщений, прежде чем ошибок. 
  
 **DeleteMessages** возвращает MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND, в зависимости от реализации хранилища сообщений. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnDeleteSelectedItem  <br/> |Mfcmapi (en) метод **IMAPIFolder::DeleteMessages** используется для удаления указанного сообщений.  <br/> |
   
## <a name="see-also"></a>См. также



[ENTRYID](entryid.md)
  
[ENTRYLIST](entrylist.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Обработка ошибок с помощью макросов](using-macros-for-error-handling.md)

