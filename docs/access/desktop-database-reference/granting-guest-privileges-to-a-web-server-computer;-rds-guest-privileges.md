---
title: Предоставление гостевых привилегий компьютеру веб-сервера; Гостевых привилегий RDS
TOCTitle: Granting guest privileges to a web server computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0ee29125bf06ef51d1ac511838bdd09231e1a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292127"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="af1cc-102">Предоставление гостевых привилегий компьютеру с веб-сервером; Гостевых привилегий RDS</span><span class="sxs-lookup"><span data-stu-id="af1cc-102">Granting guest privileges to a web server computer; RDS guest privileges</span></span>

<span data-ttu-id="af1cc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="af1cc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="af1cc-104">Учетная запись анонимного веб-сервера (IUSR ComputerName) должна быть добавлена в локализованную группу "Гости" на компьютере веб-сервера для \_ использования RDS.</span><span class="sxs-lookup"><span data-stu-id="af1cc-104">The anonymous web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the web server computer to use RDS.</span></span>

<span data-ttu-id="af1cc-105">**Предоставление гостевых привилегий компьютеру веб-сервера**</span><span class="sxs-lookup"><span data-stu-id="af1cc-105">**To grant guest privileges to a web server computer**</span></span>

1.  <span data-ttu-id="af1cc-106">На компьютере с Microsoft Windows 2000 Server нажмите кнопку **"Начните"** и выберите пункты "Программы", "Администрирование" и "Управление   **компьютером".**</span><span class="sxs-lookup"><span data-stu-id="af1cc-106">On your Microsoft Windows 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="af1cc-107">В дереве консоли в области **"Локальные пользователи и группы"** щелкните **"Группы".**</span><span class="sxs-lookup"><span data-stu-id="af1cc-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="af1cc-108">Выберите **локализованную группу "Гости".**</span><span class="sxs-lookup"><span data-stu-id="af1cc-108">Select the **Guests** local group.</span></span> <span data-ttu-id="af1cc-109">В меню **"Действие"** выберите **"Свойства".**</span><span class="sxs-lookup"><span data-stu-id="af1cc-109">From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="af1cc-110">В **диалоговом окне "Свойства** гостей" нажмите кнопку **"Добавить".**</span><span class="sxs-lookup"><span data-stu-id="af1cc-110">In the **Guests Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="af1cc-111">Если учетная запись анонимного веб-сервера  не появляется в списке в диалоговом окне "Выбор пользователей или групп", введите ее имя (IUSR \_ *ComputerName)* в нижнее пустое поле и нажмите кнопку **"Добавить".**</span><span class="sxs-lookup"><span data-stu-id="af1cc-111">If the anonymous web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>

6.  <span data-ttu-id="af1cc-112">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="af1cc-112">Click **OK**.</span></span>

