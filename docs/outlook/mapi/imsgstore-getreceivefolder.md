---
title: IMsgStoreGetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolder
api_type:
- COM
ms.assetid: ccd9d623-a3cb-4e66-9649-78c3887cb726
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a8cd211cc16b620ac47357271070e0b45b867bea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579944"
---
# <a name="imsgstoregetreceivefolder"></a>IMsgStore::GetReceiveFolder

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Получает к папке, где были установлены как место назначения для входящих сообщений из указанного класса сообщений или по умолчанию получают папки для хранения сообщений.
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a>Параметры

 _lpszMessageClass_
  
> [in] Указатель на класс сообщений, который связан с папкой получения. Если параметр _lpszMessageClass_ имеет значение NULL или пустая строка, **GetReceiveFolder** возвращает значение по умолчанию получают папки для хранения сообщений. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип переданное и возвращенных строк. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> — Это строка класс сообщения в формате Юникод. Если флаг MAPI_UNICODE не установлен, — это строка класс сообщения в формате ANSI.
    
 _lpcbEntryID_
  
> [out] Указатель на число байтов в идентификатор записи, на который указывает параметр _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Указатель на указатель на идентификатор записи для запрошенного получать папку.
    
 _lppszExplicitClass_
  
> [out] Указатель на указатель на класс сообщения, явно задает в качестве его получать папку папке указывает _lppEntryID_. Этот класс сообщения должны быть то же, что класс с помощью параметра _lpszMessageClass_ или базового класса этого класса. Значение NULL указывает, что папка, на который указывает _lppEntryID_ по умолчанию получают папки для хранения сообщений. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Папку получения успешно возвращен.
    
## <a name="remarks"></a>Замечания

Метод **IMsgStore::GetReceiveFolder** Получает идентификатор записи папки получения, папки, предназначенный для получения входящих сообщений класса определенного сообщения. С помощью параметра _lpszMessageClass_ абонентов можно указать класс сообщения или значение NULL. Если _lpszMessageClass_ имеет значение NULL, **GetReceiveFolder** возвращает следующие значения: 
  
- В _lppszExplicitClass_имя класса первоначального базового класса сообщений указывает явно задать папку получения _lpszMessageClass_ . 
    
- В _lppEntryID_идентификатор записи папки получения для базового класса, на который указывает с помощью параметра _lppszExplicitClass_ . 
    
Предположим, например, папку получения класс сообщения **IPM. Примечание** имеет значение записи идентификатор папки "Входящие" и **GetReceiveFolder** вызывается с содержимым _lpszMessageClass_ значение **IPM. Note.Phone**. Если **IPM. Note.Phone** не имеют явно получает набор папок, **GetReceiveFolder** возвращает идентификатор записи из папки «Входящие» в _lppEntryID_ и **IPM. Примечание** в _lppszExplicitClass_.
  
Если клиент вызывает **GetReceiveFolder** для класса сообщений и не установлен в папку получения для этого класса сообщений, _lppszExplicitClass_ — это строка нулевой длины, string в формате Юникод или строку в формате ANSI в зависимости от того, требуется ли клиент задан флаг MAPI_UNICODE в параметре _ulFlags_ . 
  
По умолчанию получение папки, полученного с передачей NULL в параметре _lpszMessageClass_ , всегда существует для каждого хранилища сообщений. 
  
Клиента необходимо вызвать функцию [MAPIFreeBuffer](mapifreebuffer.md) , когда это делается с идентификатором записи, возвращаемых в _lppEntryID_ , чтобы освободить память, в котором размещается этот идентификатор записи. Он также вызвать **MAPIFreeBuffer** при завершении со строки класс сообщения, возвращаемые в _lppszExplicitClass_ , чтобы освободить память, в котором размещается этой строки. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetInbox  <br/> |Mfcmapi (en) использует метод **IMsgStore::GetReceiveFolder** найти папку "Входящие".  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

