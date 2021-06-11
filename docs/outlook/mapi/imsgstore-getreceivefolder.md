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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получает папку, которая была установлена в качестве назначения для входящих сообщений указанного класса сообщений или в качестве папки получения по умолчанию для магазина сообщений.
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a>Parameters

 _lpszMessageClass_
  
> [in] Указатель на класс сообщений, связанный с папкой получения. Если параметр  _lpszMessageClass_ задан для NULL или пустой строки, **GetReceiveFolder** возвращает папку получения по умолчанию для магазина сообщений. 
    
 _ulFlags_
  
> [in] Битмашка флагов, которые контролируют тип переданных и возвращенных строк. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строка класса сообщения находится в формате Unicode. Если флаг MAPI_UNICODE не установлен, строка класса сообщения находится в формате ANSI.
    
 _lpcbEntryID_
  
> [вышел] Указатель на количество byte в идентификаторе входа, на который указывает параметр _lppEntryID._ 
    
 _lppEntryID_
  
> [вышел] Указатель на указатель на идентификатор записи для запрашиваемой папки получения.
    
 _lppszExplicitClass_
  
> [вышел] Указатель на указатель класса сообщений, который явно задает в качестве папки получения папку, на которую указывает _lppEntryID._ Этот класс сообщений должен быть таким же, как класс в параметре  _lpszMessageClass,_ или базовым классом этого класса. Передача NULL указывает, что папка, на которую указывает  _lppEntryID,_ является папкой получения по умолчанию для магазина сообщений. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Папка получения успешно возвращена.
    
## <a name="remarks"></a>Примечания

Метод **IMsgStore::GetReceiveFolder** получает идентификатор входа папки получения, папки, предназначенной для получения входящих сообщений определенного класса сообщений. Звонители могут указать класс сообщения или NULL в _параметре lpszMessageClass._ Если  _lpszMessageClass_ является NULL, **GetReceiveFolder** возвращает следующие значения: 
  
- В  _lppszExplicitClass_ имя первого базового класса класса сообщений, на которое указывает  _lpszMessageClass,_ явно устанавливая папку получения. 
    
- В _lppEntryID_ идентификатор записи папки получения для базового класса указывается _параметром lppszExplicitClass._ 
    
Например, предположим, что папка **IPM класса сообщений принимается. Примечание** установлено для идентификатора входа в почтовый ящик, и **GetReceiveFolder** называется с содержимым _lpszMessageClass,_ установленным **для IPM. Примечание. Телефон**. Если **IPM. Примечание. Телефон** не имеет явного набора папок получения, **GetReceiveFolder** возвращает идентификатор входа в папке "Входящие" в _lppEntryID_ и **IPM. Примечание** в _lppszExplicitClass_.
  
Если клиент вызывает **GetReceiveFolder** для класса сообщений и не задает папку получения для этого класса сообщений, _lppszExplicitClass_ — это строка нулевой длины, строка в формате Unicode или строка в формате ANSI в зависимости от того, установил ли клиент флаг MAPI_UNICODE в параметре _ulFlags._ 
  
Папка получения по умолчанию, полученная путем передачи NULL в  _параметре lpszMessageClass,_ всегда существует для каждого магазина сообщений. 
  
Клиент должен вызвать функцию [MAPIFreeBuffer,](mapifreebuffer.md) когда она будет сделана с идентификатором записи, возвращенным  _в lppEntryID,_ чтобы освободить память, которая содержит этот идентификатор записи. Следует также вызвать **MAPIFreeBuffer,** когда это будет сделано со строкой класса сообщений, возвращаемой в  _lppszExplicitClass,_ чтобы освободить память, которая содержит эту строку. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetInbox  <br/> |MFCMAPI использует **метод IMsgStore::GetReceiveFolder** для обнаружения папки "Входящие".  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

