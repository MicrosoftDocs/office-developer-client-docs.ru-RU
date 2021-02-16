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
ms.openlocfilehash: ab21dcfb9011b675e3db4e4df29cb6ecafa6e7c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435350"
---
# <a name="imsgstoregetreceivefolder"></a>IMsgStore::GetReceiveFolder

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Получает папку, которая была установлена в качестве места назначения для входящих сообщений указанного класса сообщений или в качестве папки получения по умолчанию для хранения сообщений.
  
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
  
> [in] Указатель на класс сообщения, связанный с папкой получения. Если для  _параметра lpszMessageClass_ установлено значение NULL или пустая строка, **GetReceiveFolder** возвращает папку получения по умолчанию для хранения сообщений. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом переданных и возвращенных строк. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строка класса сообщения имеет формат Юникод. Если флаг MAPI_UNICODE не установлен, строка класса сообщения имеет формат ANSI.
    
 _lpcbEntryID_
  
> [out] Указатель на количество byte в идентификаторе записи, на который указывает параметр _lppEntryID._ 
    
 _lppEntryID_
  
> [out] Указатель на указатель на идентификатор записи для запрашиваемой папки получения.
    
 _lppszExplicitClass_
  
> [out] Указатель на указатель на класс сообщения, который явным образом задает в качестве папки получения папку, на которую указывает _lppEntryID._ Этот класс сообщения должен либо быть таким же, как класс в параметре  _lpszMessageClass,_ либо базовым классом этого класса. Передача значения NULL означает, что папка, на которую указывает  _lppEntryID,_ является папкой получения по умолчанию для хранения сообщений. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Папка получения успешно возвращена.
    
## <a name="remarks"></a>Примечания

Метод **IMsgStore::GetReceiveFolder** получает идентификатор записи папки получения, папки, предназначенной для получения входящих сообщений определенного класса сообщений. Вызыватели могут указать класс сообщения или NULL в _параметре lpszMessageClass._ Если  _lpszMessageClass_ имеет значение NULL, **GetReceiveFolder** возвращает следующие значения: 
  
- В  _lppszExplicitClass_ имя первого базового класса класса сообщений, на который указывает  _lpszMessageClass,_ который явным образом указывает папку получения. 
    
- В _lppEntryID_ идентификатор записи папки получения для базового класса, на который указывает параметр _lppszExplicitClass._ 
    
Например, предположим, что папка получения IPM класса **сообщений.** Заметим, что для идентификатора записи "Входящие" вызвано значение **GetReceiveFolder,** для содержимого  _lpszMessageClass_ установлено значение **IPM. Note.Phone**. Если **IPM. Note.Phone** does not have an explicit receive folder set, **GetReceiveFolder** returns the entry identifier of the Inbox in _lppEntryID_ and **IPM. Примечание** в _lppszExplicitClass._
  
Если клиент вызывает **GetReceiveFolder** для класса сообщения и не установил папку получения для этого класса сообщений, _lppszExplicitClass_ — это строка нулевой длины, строка в формате Юникод или строка в формате ANSI в зависимости от того, установил ли клиент флаг MAPI_UNICODE в параметре _ulFlags._ 
  
Папка получения по умолчанию, полученная путем передачи значения NULL в  _параметре lpszMessageClass,_ всегда существует для каждого хранения сообщений. 
  
Клиент должен вызывать функцию [MAPIFreeBuffer,](mapifreebuffer.md) когда это делается с идентификатором записи, возвращенным  _в lppEntryID,_ чтобы освободить память, которая содержит этот идентификатор записи. Он также должен вызывать **MAPIFreeBuffer,** когда это делается со строкой класса сообщения, возвращаемой  _в lppszExplicitClass,_ чтобы освободить память, которая содержит эту строку. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetInbox  <br/> |MFCMAPI использует метод **IMsgStore::GetReceiveFolder** для поиска папки "Входящие".  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

