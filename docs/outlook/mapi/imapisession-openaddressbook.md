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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает интегрированную адресную книгу MAPI, возвращая указатель [IAddrBook](iaddrbookimapiprop.md) для дальнейшего доступа. 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Handle to the parent window of the common address dialog box and other related displays.
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, используемый для доступа к адресной книге. Передача **null** возвращает указатель на стандартный интерфейс адресной книги [IAddrBook : IMAPIProp](iaddrbookimapiprop.md). 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет открытием адресной книги. Можно установить следующий флаг:
    
AB_NO_DIALOG 
  
> Подавляет отображение диалогов. Если флаг AB_NO_DIALOG не установлен, поставщики адресных книг, внося вклад в интегрированную адресную книгу, могут задействовать у пользователя все необходимые сведения. 
    
 _lppAdrBook_
  
> [out] Указатель на указатель на адресную книгу.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Адресная книга успешно открыта.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов был успешным, но не удалось открыть контейнеры одного или более поставщиков адресных книг. При возвращении этого предупреждения вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **макрос HR_FAILED.** Дополнительные сведения см. в [теме "Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::OpenAddressBook** открывает интегрированную адресную книгу MAPI, коллекцию контейнеров верхнего уровня всех поставщиков адресных книг в профиле. Указатель, который возвращается в  _параметре lppAdrBook,_ обеспечивает дополнительный доступ к содержимому адресной книги. Это позволяет вызываемой службе выполнять такие задачи, как открытие отдельных контейнеров, поиск пользователей сообщений и отображение общих диалогов адресов. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **OpenAddressBook** возвращает MAPI_W_ERRORS_RETURNED, если не удается загрузить одного или несколько поставщиков адресных книг в профиле. Это значение является предупреждением, а не значением ошибки; обрабатывать его так же, как S_OK. **OpenAddressBook** всегда возвращает допустимый указатель в  _параметре lppAdrBook_ независимо от того, сколько поставщиков адресной книги не удалось загрузить. Поэтому перед выходом из журнала необходимо всегда вызывать метод [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) адресной книги. 
  
Когда **OpenAddressBook** возвращает MAPI_W_ERRORS_RETURNED, вызовите [IMAPISession::GetLastError,](imapisession-getlasterror.md) чтобы получить структуру [MAPIERROR,](mapierror.md) которая содержит сведения о сбойных поставщиках. Возвращается **одна структура MAPIERROR,** которая содержит сведения, предоставленные всеми поставщиками. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetAddrBook  <br/> |MFCMAPI использует метод **IMAPISession::OpenAddressBook** для получения интегрированной адресной книги.  <br/> |
   
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

