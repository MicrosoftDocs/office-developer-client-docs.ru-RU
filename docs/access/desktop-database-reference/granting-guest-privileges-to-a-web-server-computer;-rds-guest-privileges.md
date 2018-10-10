---
title: Предоставление гостевой привилегии на компьютере веб-сервера; Привилегии гостевой служб удаленных рабочих СТОЛОВ
TOCTitle: Granting Guest Privileges to a Web Server Computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7d09de280c9edcfdf4305bb6c2ba09aa01e556ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481735"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="901d3-102">Предоставление гостевой привилегии на компьютере веб-сервера; Привилегии гостевой служб удаленных рабочих СТОЛОВ</span><span class="sxs-lookup"><span data-stu-id="901d3-102">Granting Guest Privileges to a Web Server Computer; RDS guest privileges</span></span> 


<span data-ttu-id="901d3-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="901d3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="901d3-104">Учетной записи анонимного Web server (IUSR\_*ComputerName*) необходимо добавить Гости локальной группы на компьютере веб-сервера для использования RDS.</span><span class="sxs-lookup"><span data-stu-id="901d3-104">The anonymous Web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the Web server computer to use RDS.</span></span>

<span data-ttu-id="901d3-105">**Для предоставления прав гостя на компьютере веб-сервера**</span><span class="sxs-lookup"><span data-stu-id="901d3-105">**To grant guest privileges to a Web server computer**</span></span>

1.  <span data-ttu-id="901d3-106">На компьютере сервера Microsoft Windows® 2000 нажмите кнопку **Пуск**, выберите пункты **программы**, **Администрирование**и выберите команду **Управление компьютером**.</span><span class="sxs-lookup"><span data-stu-id="901d3-106">On your Microsoft Windows® 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="901d3-107">В дереве консоли в **Локальные пользователи и группы**щелкните **группы**.</span><span class="sxs-lookup"><span data-stu-id="901d3-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="901d3-108">Выберите группу локальных **Гости** .</span><span class="sxs-lookup"><span data-stu-id="901d3-108">Select the **Guests** local group.</span></span> <span data-ttu-id="901d3-109">В меню **Действие** выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="901d3-109">From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="901d3-110">В диалоговом окне **Свойства Гости** нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="901d3-110">In the **Guests Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="901d3-111">Если учетной записи анонимного Web server не отображается в списке в диалоговом окне **Выбор пользователей или групп** , введите его имя (IUSR\_*ComputerName*) в нижней пустой, а затем щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="901d3-111">If the anonymous Web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>

6.  <span data-ttu-id="901d3-112">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="901d3-112">Click **OK**.</span></span>

