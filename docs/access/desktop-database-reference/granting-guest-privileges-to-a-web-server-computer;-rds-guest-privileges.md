---
title: Предоставление гостевой привилегии на компьютере веб-сервера; Привилегии гостевой служб удаленных рабочих СТОЛОВ
TOCTitle: Granting Guest Privileges to a Web Server Computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bee4c05e3adc0fa3ad722b5c82c63f315860e12c
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604115"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="ee451-102">Предоставление гостевой привилегии на компьютере веб-сервера; Привилегии гостевой служб удаленных рабочих СТОЛОВ</span><span class="sxs-lookup"><span data-stu-id="ee451-102">Granting Guest Privileges to a Web Server Computer; RDS guest privileges</span></span> 


<span data-ttu-id="ee451-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee451-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ee451-104"><<<<<<< HEAD учетной записи анонимного Web server (IUSR\_*ComputerName*) необходимо добавить Гости локальной группы на компьютере веб-сервера для использования RDS.</span><span class="sxs-lookup"><span data-stu-id="ee451-104"><<<<<<< HEAD The anonymous Web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the Web server computer to use RDS.</span></span>

<a name="to-grant-guest-privileges-to-a-web-server-computer"></a><span data-ttu-id="ee451-105">**Для предоставления прав гостя на компьютере веб-сервера**</span><span class="sxs-lookup"><span data-stu-id="ee451-105">**To grant guest privileges to a Web server computer**</span></span>
=======
<span data-ttu-id="ee451-106">Учетная запись сервера анонимного веб-узла (IUSR\_*ComputerName*) необходимо добавить Гости локальной группы на компьютере веб-сервера для использования RDS.</span><span class="sxs-lookup"><span data-stu-id="ee451-106">The anonymous web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the web server computer to use RDS.</span></span>

<span data-ttu-id="ee451-107">**Для предоставления прав гостя на компьютере веб-сервера**</span><span class="sxs-lookup"><span data-stu-id="ee451-107">**To grant guest privileges to a web server computer**</span></span>
>>>>>>> <span data-ttu-id="ee451-108">master</span><span class="sxs-lookup"><span data-stu-id="ee451-108">master</span></span>

1.  <span data-ttu-id="ee451-109">На компьютере сервера Microsoft Windows® 2000 нажмите кнопку **Пуск**, выберите пункты **программы**, **Администрирование**и выберите команду **Управление компьютером**.</span><span class="sxs-lookup"><span data-stu-id="ee451-109">On your Microsoft Windows® 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="ee451-110">В дереве консоли в **Локальные пользователи и группы**щелкните **группы**.</span><span class="sxs-lookup"><span data-stu-id="ee451-110">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="ee451-111">Выберите группу локальных **Гости** .</span><span class="sxs-lookup"><span data-stu-id="ee451-111">Select the **Guests** local group.</span></span> <span data-ttu-id="ee451-112">В меню **Действие** выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="ee451-112">From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="ee451-113">В диалоговом окне **Свойства Гости** нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="ee451-113">In the **Guests Properties** dialog box, click **Add**.</span></span>

<span data-ttu-id="ee451-114"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="ee451-114"><<<<<<< HEAD</span></span>
5.  <span data-ttu-id="ee451-115">Если учетной записи анонимного Web server не отображается в списке в диалоговом окне **Выбор пользователей или групп** , введите его имя (IUSR\_*ComputerName*) в нижней пустой, а затем щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="ee451-115">If the anonymous Web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>
=======
5.  <span data-ttu-id="ee451-116">Если учетной записи анонимного веб-узла сервера не отображается в списке в диалоговом окне **Выбор пользователей или групп** , введите его имя (IUSR\_*ComputerName*) в нижней пустой, а затем щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="ee451-116">If the anonymous web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>
>>>>>>> <span data-ttu-id="ee451-117">master</span><span class="sxs-lookup"><span data-stu-id="ee451-117">master</span></span>

6.  <span data-ttu-id="ee451-118">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ee451-118">Click **OK**.</span></span>

