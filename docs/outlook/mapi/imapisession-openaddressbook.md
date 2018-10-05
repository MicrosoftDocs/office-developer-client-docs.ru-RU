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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396976"
---
# <a name="imapisessionopenaddressbook"></a>IMAPISession::OpenAddressBook

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает интегрированной адресной книги MAPI, возвращает указатель [IAddrBook](iaddrbookimapiprop.md) для дальнейшей доступа. 
  
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
  
> [in] Дескриптор родительского окна стандартным диалоговым окном адрес и других, связанных с отображает.
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к адресной книге. Передача **значения null** возвращает указатель на стандартный интерфейс в адресной книге, [IAddrBook: IMAPIProp](iaddrbookimapiprop.md). 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет открывающий адресной книги. Можно задать следующий флаг:
    
AB_NO_DIALOG 
  
> Запрещает отображение диалоговых окон. Если флаг AB_NO_DIALOG не установлен, поставщиками адресных книг, которые используются в интегрированной адресной книги может запрашивать у пользователя все необходимые сведения. 
    
 _lppAdrBook_
  
> [out] Указатель на указатель в адресной книге.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> В адресной книге, был успешно открыт.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов завершился успешно, но не удается открыть контейнеров один или несколько поставщиками адресной книги. При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Замечания

Метод **IMAPISession::OpenAddressBook** открывает интегрированной адресной книги MAPI, семейства сайтов верхнего уровня контейнеров всех поставщиками адресной книги в профиле. Указатель, который возвращается в параметре _lppAdrBook_ дальнейшей предоставляет доступ к содержимому в адресной книге. Это позволяет для выполнения задач, таких как открывающий отдельными контейнеры, обмена мгновенными сообщениями пользователи поиск и отображение общие диалоговые окна адрес звонящего. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **OpenAddressBook** возвращает MAPI_W_ERRORS_RETURNED, если не удается загрузить один или несколько поставщиками адресной книги в профиле. Это значение — это предупреждение не значением ошибки; обработать его как значение S_OK. **OpenAddressBook** всегда возвращает указатель на допустимый в параметре _lppAdrBook_ , независимо от того, сколько поставщиками адресной книги не удалось загрузить. Таким образом всегда вызовите метод [функции IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) адресной книги к определенному моменту перед выходом из системы. 
  
При **OpenAddressBook** возвращает MAPI_W_ERRORS_RETURNED, вызовите [IMAPISession::GetLastError](imapisession-getlasterror.md) для получения [MAPIERROR](mapierror.md) структура, содержащая сведения о поставщиках со сбоями. Возвращается один **MAPIERROR** структуры, которая содержит сведения, предоставленные всех поставщиков. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetAddrBook  <br/> |Mfcmapi (en) использует метод **IMAPISession::OpenAddressBook** для получения интегрированной адресной книги.  <br/> |
   
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

