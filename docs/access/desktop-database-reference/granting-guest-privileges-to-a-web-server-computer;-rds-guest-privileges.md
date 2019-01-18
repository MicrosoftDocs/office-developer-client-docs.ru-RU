---
title: Предоставление права гостевой на компьютере веб-сервера; Привилегии гостевой служб удаленных рабочих СТОЛОВ
TOCTitle: Granting guest privileges to a web server computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0ee29125bf06ef51d1ac511838bdd09231e1a6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700551"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="1cfc6-102">Предоставление права гостевой на компьютере веб-сервера; Привилегии гостевой служб удаленных рабочих СТОЛОВ</span><span class="sxs-lookup"><span data-stu-id="1cfc6-102">Granting guest privileges to a web server computer; RDS guest privileges</span></span>

<span data-ttu-id="1cfc6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1cfc6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1cfc6-104">Учетная запись сервера анонимного веб-узла (IUSR\_*ComputerName*) необходимо добавить Гости локальной группы на компьютере веб-сервера для использования RDS.</span><span class="sxs-lookup"><span data-stu-id="1cfc6-104">The anonymous web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the web server computer to use RDS.</span></span>

<span data-ttu-id="1cfc6-105">**Для предоставления прав гостя на компьютере веб-сервера**</span><span class="sxs-lookup"><span data-stu-id="1cfc6-105">**To grant guest privileges to a web server computer**</span></span>

1.  <span data-ttu-id="1cfc6-106">На компьютере Microsoft Windows 2000 Server нажмите кнопку **Пуск**, выберите пункты **программы**, **Администрирование**и выберите команду **Управление компьютером**.</span><span class="sxs-lookup"><span data-stu-id="1cfc6-106">On your Microsoft Windows 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="1cfc6-107">В дереве консоли в **Локальные пользователи и группы**щелкните **группы**.</span><span class="sxs-lookup"><span data-stu-id="1cfc6-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="1cfc6-108">Выберите группу локальных **Гости** .</span><span class="sxs-lookup"><span data-stu-id="1cfc6-108">Select the **Guests** local group.</span></span> <span data-ttu-id="1cfc6-109">В меню **Действие** выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="1cfc6-109">From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="1cfc6-110">В диалоговом окне **Свойства Гости** нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="1cfc6-110">In the **Guests Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="1cfc6-111">Если учетной записи анонимного веб-узла сервера не отображается в списке в диалоговом окне **Выбор пользователей или групп** , введите его имя (IUSR\_*ComputerName*) в нижней пустой, а затем щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="1cfc6-111">If the anonymous web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>

6.  <span data-ttu-id="1cfc6-112">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1cfc6-112">Click **OK**.</span></span>

