---
title: IAddrBookSetDefaultDir
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

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи контейнера адресной книги по умолчанию.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Контейнер адресной книги по умолчанию был успешно установлен.
    
## <a name="remarks"></a>Примечания

Клиенты и поставщики услуг называют **метод SetDefaultDir** для создания нового контейнера адресной книги по умолчанию. Контейнер по умолчанию — это контейнер, который пользователь видит в адресной книге при первом открывании адресной книги. **SetDefaultDir** сохраняет контейнер по умолчанию в качестве записи в профиле. Контейнер остается по умолчанию до тех пор, пока в том же сеансе или на другом сеансе не будет выполнен другой вызов **в SetDefaultDir** или не будет удален контейнер. 
  
> [!NOTE]
> Свойство [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) соответствует параметру **Выберите** автоматически в диалоговом окте "Параметры адресной книги". Если это свойство существует в [разделе IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) профиля и задано значение **true,** диалоговое окно адресной книги больше не по умолчанию подходит для контейнера, указанного **SetDefaultDir,** но выбирает адресную книгу, которую Microsoft Outlook считает подходящей для контекста, в котором диалоговое окно отображалось. Обратите внимание, что это может привести к плохому опыту сторонних поставщиков адресных книг. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Abcontdlg.cpp  <br/> |CAbContDlg::OnSetDefaultDir  <br/> |MFCMAPI использует метод **SetDefaultDir,** чтобы сделать указанный контейнер адресной книги по умолчанию.  <br/> |
   
## <a name="see-also"></a>См. также



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[IMAPISession::Logoff](imapisession-logoff.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

