---
title: Открытие адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79e0bc93-f37d-4f6a-beed-7519d01e0056
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 4b9d7b8cf71b4e00dac6022e1dda727ef7a23036
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810061"
---
# <a name="opening-the-address-book"></a><span data-ttu-id="a6e1d-103">Открытие адресной книги</span><span class="sxs-lookup"><span data-stu-id="a6e1d-103">Opening the address book</span></span>

<span data-ttu-id="a6e1d-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a6e1d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a6e1d-p101">Call [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to open the integrated address book and retrieve a pointer to the MAPI [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) interface. The methods of the **IAddrBook** interface can be used to access entries in all of the containers of each of the address book providers in the profile.</span><span class="sxs-lookup"><span data-stu-id="a6e1d-p101">Call [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to open the integrated address book and retrieve a pointer to the MAPI [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface. The methods of the **IAddrBook** interface can be used to access entries in all of the containers of each of the address book providers in the profile.</span></span> 
  
<span data-ttu-id="a6e1d-p102">**OpenAddressBook** might return a warning, MAPI_W_ERRORS_RETURNED, to indicate that there were problems with one or more of the address book providers. Interactive clients should call [IMAPISession::GetLastError](imapisession-getlasterror.md) to retrieve additional error information and display the returned information the first time they call **OpenAddressBook** and it returns a warning.</span><span class="sxs-lookup"><span data-stu-id="a6e1d-p102">**OpenAddressBook** might return a warning, MAPI_W_ERRORS_RETURNED, to indicate that there were problems with one or more of the address book providers. Interactive clients should call [IMAPISession::GetLastError](imapisession-getlasterror.md) to retrieve additional error information and display the returned information the first time they call **OpenAddressBook** and it returns a warning.</span></span> 
  
<span data-ttu-id="a6e1d-p103">��������������� �������� ������� ������������ �������������� � ���������� ������, ���� ����� �������� �������. ��������� ������������ **IAddrBook** �������� ���������� ���������� �� ����, ��������� �� ��� ��� ����������� ��������� ��� �� ���� �� ������������ �������� ����� � �������. ����� ������� ������������� � ��������������� ������� ������ ��������� ������� ��� ������������ ��������� **IAddrBook** ��� ���������� ������.</span><span class="sxs-lookup"><span data-stu-id="a6e1d-p103">Noninteractive clients should ignore the warning and proceed as if the method succeeded. The returned **IAddrBook** interface is valid regardless of whether all, some, or none of the address book providers in the profile are running. Therefore, both interactive and noninteractive clients must always remember to release the **IAddrBook** pointer when the session ends.</span></span> 
  

