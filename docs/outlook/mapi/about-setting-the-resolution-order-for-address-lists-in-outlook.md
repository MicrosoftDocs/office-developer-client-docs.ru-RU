---
title: � ��������� ��������� ���������� ��� ������� ������� � Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: '���� ���������� ���������: 5 ���� 2012 �.'
ms.openlocfilehash: 22d56ffac5d9d628b04e364fa772ddc8de488a31
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578656"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a><span data-ttu-id="db509-103">� ��������� ��������� ���������� ��� ������� ������� � Outlook</span><span class="sxs-lookup"><span data-stu-id="db509-103">About Setting the Resolution Order for Address Lists in Outlook</span></span>

  
  
<span data-ttu-id="db509-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db509-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db509-105">Для каждого профиля Microsoft Office Outlook поддерживает несколько списков адресов и пользователи могут вручную задать порядок списков адресов в список получателей электронной почты разрешаются сообщений и участниками в рабочей области приглашений на собрания.</span><span class="sxs-lookup"><span data-stu-id="db509-105">For each profile, Microsoft Office Outlook supports multiple address lists and users can manually specify the order of address lists by which recipients in email messages and attendees in meeting requests are resolved.</span></span> <span data-ttu-id="db509-106">�������� ����� ������ ������� ���������, ����� ����� ����������� ������� �������� ����� Outlook � ����� � ���������� ������ �������.</span><span class="sxs-lookup"><span data-stu-id="db509-106">For example, you can set the resolution order so that names are resolved first against your Outlook Address Book, and then against the Global Address List.</span></span> <span data-ttu-id="db509-107">�� ���������� ������������ ����� ������� �������� �����, ������� ������ **������** � �������� **���������**, ����� ������� ���� ������� ���������.</span><span class="sxs-lookup"><span data-stu-id="db509-107">On a computer, a user can open the Address Book, click **Tools** and then **Options** to specify this resolution order.</span></span> <span data-ttu-id="db509-108">��� �� ����� � ������������� �����, ����� ����������� ��� ��-��������������� ���������� �������� ������� ������� �������, ������� ����������� �����.</span><span class="sxs-lookup"><span data-stu-id="db509-108">However, in a corporate environment, it is more efficient for IT administrators to programmatically set the order of address lists by which names are resolved.</span></span> <span data-ttu-id="db509-109">����� ��� ����� ������������ � �������� ����� ������� �������� �������������, ������������� ������������ ������ �����������.</span><span class="sxs-lookup"><span data-stu-id="db509-109">Such code can be used as part of a startup automation script that an administrator deploys inside the corporation.</span></span> 
  
<span data-ttu-id="db509-p102">����� **[SetSearchPath](iaddrbook-getsearchpath.md)** ������������ MAPI � ��������� **[IAddrBook](iaddrbookimapiprop.md)**, ������� ��������� ������ ����� ���� ��� ������ �������, ������� ������������ ��� ���������� ����. ������������� ������ **IAddrBook::SetSearchPath**, ���������� ������� ������� ����������� ���������� � ������� ������, ���������� ����������� ������ ����� ���� � �������, � ������� ��� ������ ���� ���������. ������ ������ � ���� ������ ������ ����� ��������� ������������� ������ ��������������� �������� �����.</span><span class="sxs-lookup"><span data-stu-id="db509-p102">MAPI supports the **[SetSearchPath](iaddrbook-getsearchpath.md)** method in the **[IAddrBook](iaddrbookimapiprop.md)** interface, which allows you to set a new search path in the profile that is used for name resolution. To use the **IAddrBook::SetSearchPath** method, you must specify the desired resolution order by using an array that holds containers of the relevant address books in the order they should be resolved. Each entry in that array should also contain the entry ID of the corresponding address book.</span></span> 
  
<span data-ttu-id="db509-113">���� ��������� ������� ����, ��� ������� ���� ������ ��� ������� �������.</span><span class="sxs-lookup"><span data-stu-id="db509-113">The following are code examples of how to specify a custom search path for address lists.</span></span>
  
- [<span data-ttu-id="db509-114">Программная установка порядка разрешения для списков адресов</span><span class="sxs-lookup"><span data-stu-id="db509-114">Programmatically Set the Resolution Order for Address Lists</span></span>](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [<span data-ttu-id="db509-115">������ ���� ������ 292590: ��� �������� ������� ���������� �������� ����� � SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="db509-115">KB 292590: How To Change Address Book Sort Order with SetSearchPath</span></span>](http://support.microsoft.com/kb/292590)
    

