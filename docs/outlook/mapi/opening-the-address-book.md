---
title: Открытие адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79e0bc93-f37d-4f6a-beed-7519d01e0056
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6d1a7e8e1d9debd7eb715bbe4958657c000f1e6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404549"
---
# <a name="opening-the-address-book"></a>Открытие адресной книги

**Относится к**: Outlook 2013 | Outlook 2016 
  
Call [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to open the integrated address book and retrieve a pointer to the MAPI [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) interface. The methods of the **IAddrBook** interface can be used to access entries in all of the containers of each of the address book providers in the profile. 
  
**OpenAddressBook** might return a warning, MAPI_W_ERRORS_RETURNED, to indicate that there were problems with one or more of the address book providers. Interactive clients should call [IMAPISession::GetLastError](imapisession-getlasterror.md) to retrieve additional error information and display the returned information the first time they call **OpenAddressBook** and it returns a warning. 
  
��������������� �������� ������� ������������ �������������� � ���������� ������, ���� ����� �������� �������. ��������� ������������ **IAddrBook** �������� ���������� ���������� �� ����, ��������� �� ��� ��� ����������� ��������� ��� �� ���� �� ������������ �������� ����� � �������. ����� ������� ������������� � ��������������� ������� ������ ��������� ������� ��� ������������ ��������� **IAddrBook** ��� ���������� ������. 
  

