---
title: IMAPISessionOpenAddressBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenAddressBook
api_type:
- COM
ms.assetid: 2b6a4c6a-bb71-4ea1-a3b6-90a2722880fb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 51bf5f8455d4cb790d0c955e96249b0f9deef1af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329423"
---
# <a name="imapisessionopenaddressbook"></a>IMAPISession::OpenAddressBook

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает интегрированную адресную книгу MAPI, возвращая указатель [IAddrBook](iaddrbookimapiprop.md) для дальнейшего доступа. 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Ручка родительского окна общего диалогового окна адресов и других связанных дисплеев.
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к адресной книге. Передача **null** возвращает указатель к стандартному интерфейсу адресной [книги, IAddrBook : IMAPIProp](iaddrbookimapiprop.md). 
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют открытие адресной книги. Можно установить следующий флаг:
    
AB_NO_DIALOG 
  
> Подавляет отображение диалогов. Если флаг AB_NO_DIALOG не установлен, поставщики адресных книг, которые вносят вклад в интегрированную адресную книгу, могут подсказать пользователю любую необходимую информацию. 
    
 _lppAdrBook_
  
> [вышел] Указатель на указатель на адресную книгу.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Адресная книга была успешно открыта.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов удался, но контейнеры одного или более поставщиков адресной книги не удалось открыть. Когда это предупреждение возвращается, вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::OpenAddressBook** открывает интегрированную адресную книгу MAPI, коллекцию контейнеров верхнего уровня всех поставщиков адресных книг в профиле. Указатель, возвращаемый в  _параметре lppAdrBook,_ предоставляет дополнительный доступ к содержимому адресной книги. Это позволяет вызываемой службе выполнять такие задачи, как открытие отдельных контейнеров, поиск пользователей сообщений и отображение общих диалогов адресов. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **OpenAddressBook** возвращает MAPI_W_ERRORS_RETURNED, если не удается загрузить один или несколько поставщиков адресной книги в профиле. Это значение является предупреждением, а не значением ошибки; обрабатывать его так, как S_OK. **OpenAddressBook** всегда возвращает допустимый указатель в  _параметре lppAdrBook_ независимо от того, сколько поставщиков адресной книги не удалось загрузить. Поэтому перед отключением необходимо всегда вызывать метод [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) адресной книги. 
  
Когда **OpenAddressBook** MAPI_W_ERRORS_RETURNED, позвоните [в службу IMAPISession::GetLastError,](imapisession-getlasterror.md) чтобы получить структуру [MAPIERROR,](mapierror.md) которая содержит сведения о поставщиках сбоя. Возвращается **одна структура MAPIERROR,** которая содержит сведения, предоставленные всеми поставщиками. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetAddrBook  <br/> |MFCMAPI использует **метод IMAPISession::OpenAddressBook** для получения интегрированной адресной книги.  <br/> |
   
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

