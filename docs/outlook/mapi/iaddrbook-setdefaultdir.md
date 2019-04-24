---
title: Иаддрбуксетдефаултдир
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetDefaultDir
api_type:
- COM
ms.assetid: d5d60150-15e4-41ff-bfb0-0c67e2abcacc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3ab01f189734ac30b4c027f4e5596c88031b5f99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341701"
---
# <a name="iaddrbooksetdefaultdir"></a>IAddrBook::SetDefaultDir

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Устанавливает указанный контейнер в качестве контейнера адресной книги по умолчанию.
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Параметры

 _Кбентрид_
  
> возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ . 
    
 _Лпентрид_
  
> возврата Указатель на идентификатор элемента контейнера адресной книги по умолчанию.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Контейнер адресной книги по умолчанию успешно установлен.
    
## <a name="remarks"></a>Комментарии

Клиенты и поставщики услуг вызывают метод **сетдефаултдир** для установки нового контейнера адресной книги по умолчанию. Контейнер по умолчанию — это контейнер, который видит пользователь, отображаемый в адресной книге при первом открытии адресной книги. **Сетдефаултдир** сохраняет контейнер по умолчанию в качестве записи в профиле. Контейнер по умолчанию остается неизменным до тех пор, пока не будет выполнен другой вызов **сетдефаултдир** в том же сеансе или в другом сеансе, либо контейнер удаляется. 
  
> [!NOTE]
> Свойство [пр_аб_чусе_директори_аутоматикалли](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) соответствует параметру **выбрать автоматический** параметр в диалоговом окне Параметры адресной книги. Если это свойство существует в разделе profile [иид_капоне_проф](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) и имеет значение **true**, диалоговое окно адресной книги больше не используется по умолчанию в контейнере, указанном в **сетдефаултдир**, но выбирает адресную книгу, которую считает Microsoft Outlook подходит для контекста, в котором отображается диалоговое окно. Обратите внимание, что это может привести к неудовлетворительному взаимодействию сторонних поставщиков адресных книг. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Абконтдлг. cpp  <br/> |Кабконтдлг:: Онсетдефаултдир  <br/> |MFCMAPI использует метод **сетдефаултдир** , чтобы сделать заданный контейнер адресной книги значением по умолчанию.  <br/> |
   
## <a name="see-also"></a>См. также



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[IMAPISession::Logoff](imapisession-logoff.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

