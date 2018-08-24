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
ms.openlocfilehash: 02815c60b6bfc9809871af19e922913622588fc9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584319"
---
# <a name="imapifolderdeletefolder"></a>IMAPIFolder::DeleteFolder

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Удаляет вложенной папке.
  
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
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи вложенную папку для удаления.
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна индикатор хода выполнения. Параметр _ulUIParam_ игнорируется, пока флаг FOLDER_DIALOG будет выполнен с помощью параметра _ulFlags_ . 
    
 _lpProgress_
  
> [in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения. Если в _lpProgress_передается значение NULL, поставщика хранилища сообщений отображает индикатор выполнения с помощью реализация объекта MAPI хода выполнения. Параметр _lpProgress_ используется только флаг FOLDER_DIALOG установлен в _ulFlags_.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который управляет удаления вложенной папке. Можно задать следующие флажки:
    
DEL_FOLDERS 
  
> Следует удалить все вложенные папки вложенной папке, на который указывает _lpEntryID_ . 
    
DEL_MESSAGES 
  
> Следует удалить все сообщения в папке, на который указывает _lpEntryID_ . 
    
FOLDER_DIALOG 
  
> Индикатор выполнения должен отображаться во время операции.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Указанная папка успешно удален.
    
MAPI_E_HAS_FOLDERS 
  
> Вложенной папке удаления содержит вложенные папки, не был установлен флажок DEL_FOLDERS. Вложенные папки не были удалены.
    
MAPI_E_HAS_MESSAGES 
  
> Вложенной папке удаления содержит сообщения, а не был установлен флажок DEL_MESSAGES. Вложенной папке не был удален.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов завершился успешно, но не все записи были успешно удалены. При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Замечания

Метод **IMAPIFolder::DeleteFolder** удаляет вложенной папке. По умолчанию **DeleteFolder** работает только для пустых папок, но можно использовать его успешно непустые папок, задав два флага: DEL_FOLDERS и DEL_MESSAGES. Можно удалить только пустые папки или папки, которые установить флаги DEL_FOLDERS и DEL_MESSAGES на вызов **DeleteFolder** . DEL_FOLDERS включает все вложенные папки удаляется; DEL_MESSAGES включает все сообщения в папке требуется удалить. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

При операции удаления состоит из нескольких папок, как можно выполните операцию для каждой папки. В некоторых случаях один из папки к удалению не существует или был перемещен или скопирован в другое место. Не останавливайте операции преждевременно Если произошла ошибка, которая находится за пределами элементу управления, такие как хватает памяти, недостаточно места на диске или повреждение в хранилище сообщений.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Ожидается, что эти возвращаемые значения в следующих случаях.
  
|**Условие**|**������������ ��������**|
|:-----|:-----|
|**DeleteFolder** успешно удалил все сообщения и вложенной папке.  <br/> |ЗНАЧЕНИЕ S_OK  <br/> |
|**DeleteFolder** не удалось успешно удалить все сообщения и вложенной папке.  <br/> |MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND  <br/> |
|Не удалось завершить **DeleteFolder** .  <br/> |Любое значение ошибки, за исключением MAPI_E_NOT_FOUND  <br/> |
   
Если не удается завершить **DeleteFolder** не предполагают, что работа не выполнена. **DeleteFolder** мог удалить одно или несколько сообщений и вложенные папки до появления ошибки. 
  
Если не удается удалить один или несколько вложенных папок, **DeleteFolder** возвращает MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND, в зависимости от реализации поставщика хранилища сообщений. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDeleteSelectedItem  <br/> |Mfcmapi (en) метод **IMAPIFolder::DeleteFolder** используется для удаления папок.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

