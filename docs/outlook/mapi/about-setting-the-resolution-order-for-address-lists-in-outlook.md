---
title: � ��������� ��������� ���������� ��� ������� ������� � Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: '���� ���������� ���������: 5 ���� 2012 �.'
ms.openlocfilehash: cfc640fd419ad030de6922fa61817881caa70d07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807973"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a><span data-ttu-id="6086f-103">� ��������� ��������� ���������� ��� ������� ������� � Outlook</span><span class="sxs-lookup"><span data-stu-id="6086f-103">About Setting the Resolution Order for Address Lists in Outlook</span></span>

  
  
<span data-ttu-id="6086f-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6086f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6086f-105">Для каждого профиля Microsoft Office Outlook поддерживает несколько списков адресов и пользователи могут вручную задать порядок списков адресов в список получателей электронной почты разрешаются сообщений и участниками в рабочей области приглашений на собрания.</span><span class="sxs-lookup"><span data-stu-id="6086f-105">For each profile, Microsoft Office Outlook supports multiple address lists and users can manually specify the order of address lists by which recipients in email messages and attendees in meeting requests are resolved.</span></span> <span data-ttu-id="6086f-106">�������� ����� ������ ������� ���������, ����� ����� ����������� ������� �������� ����� Outlook � ����� � ���������� ������ �������.</span><span class="sxs-lookup"><span data-stu-id="6086f-106">For example, you can set the resolution order so that names are resolved first against your Outlook Address Book, and then against the Global Address List.</span></span> <span data-ttu-id="6086f-107">�� ���������� ������������ ����� ������� �������� �����, ������� ������ **������** � �������� **���������**, ����� ������� ���� ������� ���������.</span><span class="sxs-lookup"><span data-stu-id="6086f-107">On a computer, a user can open the Address Book, click **Tools** and then **Options** to specify this resolution order.</span></span> <span data-ttu-id="6086f-108">��� �� ����� � ������������� �����, ����� ����������� ��� ��-��������������� ���������� �������� ������� ������� �������, ������� ����������� �����.</span><span class="sxs-lookup"><span data-stu-id="6086f-108">However, in a corporate environment, it is more efficient for IT administrators to programmatically set the order of address lists by which names are resolved.</span></span> <span data-ttu-id="6086f-109">����� ��� ����� ������������ � �������� ����� ������� �������� �������������, ������������� ������������ ������ �����������.</span><span class="sxs-lookup"><span data-stu-id="6086f-109">Such code can be used as part of a startup automation script that an administrator deploys inside the corporation.</span></span> 
  
<span data-ttu-id="6086f-p102">����� **[SetSearchPath](iaddrbook-getsearchpath.md)** ������������ MAPI � ��������� **[IAddrBook](iaddrbookimapiprop.md)**, ������� ��������� ������ ����� ���� ��� ������ �������, ������� ������������ ��� ���������� ����. ������������� ������ **IAddrBook::SetSearchPath**, ���������� ������� ������� ����������� ���������� � ������� ������, ���������� ����������� ������ ����� ���� � �������, � ������� ��� ������ ���� ���������. ������ ������ � ���� ������ ������ ����� ��������� ������������� ������ ��������������� �������� �����.</span><span class="sxs-lookup"><span data-stu-id="6086f-p102">MAPI supports the **[SetSearchPath](iaddrbook-getsearchpath.md)** method in the **[IAddrBook](iaddrbookimapiprop.md)** interface, which allows you to set a new search path in the profile that is used for name resolution. To use the **IAddrBook::SetSearchPath** method, you must specify the desired resolution order by using an array that holds containers of the relevant address books in the order they should be resolved. Each entry in that array should also contain the entry ID of the corresponding address book.</span></span> 
  
<span data-ttu-id="6086f-113">���� ��������� ������� ����, ��� ������� ���� ������ ��� ������� �������.</span><span class="sxs-lookup"><span data-stu-id="6086f-113">The following are code examples of how to specify a custom search path for address lists.</span></span>
  
- [<span data-ttu-id="6086f-114">Приоритет разрешения для списков адресов для задания программным путем</span><span class="sxs-lookup"><span data-stu-id="6086f-114">Programmatically Set the Resolution Order for Address Lists</span></span>](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [<span data-ttu-id="6086f-115">������ ���� ������ 292590: ��� �������� ������� ���������� �������� ����� � SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="6086f-115">KB 292590: How To Change Address Book Sort Order with SetSearchPath</span></span>](http://support.microsoft.com/kb/292590)
    

