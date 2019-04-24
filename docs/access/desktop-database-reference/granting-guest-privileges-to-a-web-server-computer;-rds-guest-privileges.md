---
title: Предоставление гостевых привилегий компьютеру веб-сервера; Гостевые привилегии RDS
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
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="f6251-102">Предоставление гостевых привилегий компьютеру веб-сервера; Гостевые привилегии RDS</span><span class="sxs-lookup"><span data-stu-id="f6251-102">Granting guest privileges to a web server computer; RDS guest privileges</span></span>

<span data-ttu-id="f6251-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6251-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6251-104">Учетная запись анонимного веб-\_сервера (IUSR*ComputerName*) должна быть добавлена в локальную группу гостей на компьютере веб-сервера для использования RDS.</span><span class="sxs-lookup"><span data-stu-id="f6251-104">The anonymous web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the web server computer to use RDS.</span></span>

<span data-ttu-id="f6251-105">**Предоставление гостевых привилегий компьютеру веб-сервера**</span><span class="sxs-lookup"><span data-stu-id="f6251-105">**To grant guest privileges to a web server computer**</span></span>

1.  <span data-ttu-id="f6251-106">На компьютере под управлением Microsoft Windows 2000 Server нажмите кнопку **Пуск**, последовательно выберите пункты **программы**, **Администрирование**и **Управление компьютером**.</span><span class="sxs-lookup"><span data-stu-id="f6251-106">On your Microsoft Windows 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="f6251-107">В дереве консоли в разделе **Локальные пользователи и группы**щелкните **группы**.</span><span class="sxs-lookup"><span data-stu-id="f6251-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="f6251-108">Выберите локальную группу " **гости** ".</span><span class="sxs-lookup"><span data-stu-id="f6251-108">Select the **Guests** local group.</span></span> <span data-ttu-id="f6251-109">В меню **действие** выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="f6251-109">From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="f6251-110">В диалоговом окне **Свойства: гости** нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="f6251-110">In the **Guests Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="f6251-111">Если анонимная учетная запись веб-сервера не отображается в списке в диалоговом окне **Выбор пользователей или групп** , введите его имя (\_IUSR*ComputerName*) в нижнем пустом поле и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="f6251-111">If the anonymous web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>

6.  <span data-ttu-id="f6251-112">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f6251-112">Click **OK**.</span></span>

