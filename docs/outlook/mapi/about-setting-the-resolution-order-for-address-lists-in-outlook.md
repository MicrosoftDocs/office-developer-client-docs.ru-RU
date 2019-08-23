---
title: Сведения о настройке порядка разрешения для списков адресов в Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: 'Дата последнего изменения: 05 июля 2012 г.'
ms.openlocfilehash: 07a4c3e90f686f291f95ff87f337b54d8bf35edc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321835"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a><span data-ttu-id="dbec4-103">Сведения о настройке порядка разрешения для списков адресов в Outlook</span><span class="sxs-lookup"><span data-stu-id="dbec4-103">About Setting the Resolution Order for Address Lists in Outlook</span></span>

  
  
<span data-ttu-id="dbec4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbec4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbec4-105">Для каждого профиля Microsoft Office Outlook поддерживает несколько списков адресов, и пользователи могут вручную задавать порядок списков адресов, по которому сопоставляются получатели в сообщениях электронной почты и участников в приглашениях на собрания.</span><span class="sxs-lookup"><span data-stu-id="dbec4-105">For each profile, Microsoft Office Outlook supports multiple address lists and users can manually specify the order of address lists by which recipients in email messages and attendees in meeting requests are resolved.</span></span> <span data-ttu-id="dbec4-106">Например вы можете задать порядок сопоставления таким образом, чтобы имена можно было сопоставлять сначала с адресной книгой Outlook, а затем с глобальным списком адресов.</span><span class="sxs-lookup"><span data-stu-id="dbec4-106">For example, you can set the resolution order so that names are resolved first against your Outlook Address Book, and then against the Global Address List.</span></span> <span data-ttu-id="dbec4-107">На компьютере откройте адресную книгу, нажав**Инструмента**, а затем **Параметры**, чтобы указать порядок сопоставления.</span><span class="sxs-lookup"><span data-stu-id="dbec4-107">On a computer, a user can open the Address Book, click **Tools** and then **Options** to specify this resolution order.</span></span> <span data-ttu-id="dbec4-108">В корпоративной среде IT-администраторам рекомендуется на программном уровне задать порядок списков адресов, по которым имена будут сопоставляться.</span><span class="sxs-lookup"><span data-stu-id="dbec4-108">However, in a corporate environment, it is more efficient for IT administrators to programmatically set the order of address lists by which names are resolved.</span></span> <span data-ttu-id="dbec4-109">Такой код можно использовать как часть сценария автоматизации запуска, который администратор развертывает для корпоративных нужд.</span><span class="sxs-lookup"><span data-stu-id="dbec4-109">Such code can be used as part of a startup automation script that an administrator deploys inside the corporation.</span></span> 
  
<span data-ttu-id="dbec4-p102">MAPI поддерживает метод \*\* [SetSearchPath](iaddrbook-getsearchpath.md) \*\* интерфейса\*\* [IAddrBook](iaddrbookimapiprop.md)\*\*, в котором вы можете указать новый путь поиска в профиле, который используется при сопоставление имени. Чтобы использовать метод **IAddrBook::SetSearchPath**, вы должны указать желаемый порядок сопоставления с помощью массива, который содержит контейнеры соответствующих адресных книг в том порядке, в каком должно производиться сопоставление. Каждая запись в этот массиве также должна содержать идентификатор записи соответствующей адресной книги.</span><span class="sxs-lookup"><span data-stu-id="dbec4-p102">MAPI supports the **[SetSearchPath](iaddrbook-getsearchpath.md)** method in the **[IAddrBook](iaddrbookimapiprop.md)** interface, which allows you to set a new search path in the profile that is used for name resolution. To use the **IAddrBook::SetSearchPath** method, you must specify the desired resolution order by using an array that holds containers of the relevant address books in the order they should be resolved. Each entry in that array should also contain the entry ID of the corresponding address book.</span></span> 
  
<span data-ttu-id="dbec4-113">Ниже приведены примеры кода, демонстрирующие указание настраиваемого пути поиска для списков адресов.</span><span class="sxs-lookup"><span data-stu-id="dbec4-113">The following are code examples of how to specify a custom search path for address lists.</span></span>
  
- [<span data-ttu-id="dbec4-114">Программная установка порядка сопоставления для списков адресов</span><span class="sxs-lookup"><span data-stu-id="dbec4-114">Programmatically Set the Resolution Order for Address Lists</span></span>](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [<span data-ttu-id="dbec4-115">Статья базы знаний 292590: Как изменить порядок сортировки адресной книги с SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="dbec4-115">KB 292590: How To Change Address Book Sort Order with SetSearchPath</span></span>](https://support.microsoft.com/kb/292590)
    

