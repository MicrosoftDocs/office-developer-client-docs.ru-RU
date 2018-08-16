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
ms.openlocfilehash: 00d5b2bfc6b0c024f0ef12ce19fed90ef0af6721
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808756"
---
# <a name="iaddrbooksetdefaultdir"></a>IAddrBook::SetDefaultDir

  
  
**Относится к**: Outlook 
  
Устанавливает указанный контейнер как контейнер адресной книги по умолчанию.
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Параметры

 _cbEntryID_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи контейнер адресной книги по умолчанию.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Контейнер адресной книги по умолчанию был успешно установлен.
    
## <a name="remarks"></a>Замечания

Клиенты и поставщики услуг вызовите метод **SetDefaultDir** , чтобы установить новый контейнер адресной книги по умолчанию. Контейнер по умолчанию является контейнером, пользователь видит отображаются в адресной книге, при первом открытии адресной книги. **SetDefaultDir** сохраняет контейнер по умолчанию, как запись в профиле. Контейнер остается по умолчанию, пока другой вызов **SetDefaultDir** выполняется в том же сеансе или в другом сеансе, либо контейнер было удалено. 
  
> [!NOTE]
> Свойство [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) соответствует параметру **автоматически выбирать** в диалоговом окне параметры адресной книги. После этого свойства в разделе профилей [IID_CAPONE_PROF](http://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) существует и имеет значение **true**, диалоговое окно адресной книге больше не параметры по умолчанию в контейнер, указанный с **SetDefaultDir**, но выбирает к адресной книге, которая учитывает Microsoft Outlook подходит для контекста, в котором диалоговое окно отображается. Обратите внимание на то, что это может привести к низкого уровня качества для поставщиками сторонних производителей адресной книги. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|Abcontdlg.cpp  <br/> |CAbContDlg::OnSetDefaultDir  <br/> |Mfcmapi (en) использует метод **SetDefaultDir** чтобы сделать контейнер указанного адресной книги по умолчанию.  <br/> |
   
## <a name="see-also"></a>См. также



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[IMAPISession::Logoff](imapisession-logoff.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
