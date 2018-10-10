---
title: Minimizing Log File Space Usage
TOCTitle: Minimizing Log File Space Usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2ac2bee2bf3f1036583bd195edc0c3da9e052f3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483090"
---
# <a name="minimizing-log-file-space-usage"></a><span data-ttu-id="d5f48-102">Minimizing Log File Space Usage</span><span class="sxs-lookup"><span data-stu-id="d5f48-102">Minimizing Log File Space Usage</span></span>


<span data-ttu-id="d5f48-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d5f48-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d5f48-104">Файл журнала можно указать быстро (таким образом, остановка работы сервера) при наличии больших объемов активности в базе данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d5f48-104">A log file may fill quickly (thus halting the server) if there is a large volume of activity on an SQL Server database.</span></span> <span data-ttu-id="d5f48-105">Файл журнала можно включить **Truncate на контрольной точки** для значительного увеличения работы файла журнала для базы данных.</span><span class="sxs-lookup"><span data-stu-id="d5f48-105">You can set the log file to **Truncate on Checkpoint** to significantly extend the life of the log file for a database.</span></span>

<span data-ttu-id="d5f48-106">**Чтобы включить Truncate на контрольной точки в Microsoft SQL Server 6.5**</span><span class="sxs-lookup"><span data-stu-id="d5f48-106">**To enable Truncate on Checkpoint in Microsoft SQL Server 6.5**</span></span>

1.  <span data-ttu-id="d5f48-107">Запустите Microsoft SQL Server Enterprise Manager, откройте дерево для сервера и откройте дерево устройств базы данных.</span><span class="sxs-lookup"><span data-stu-id="d5f48-107">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="d5f48-108">Дважды щелкните имя базы данных, на котором эта возможность включена.</span><span class="sxs-lookup"><span data-stu-id="d5f48-108">Double-click the name of the database on which this feature will be enabled.</span></span>

3.  <span data-ttu-id="d5f48-109">Вкладка " **базы данных** " выберите **Truncate**.</span><span class="sxs-lookup"><span data-stu-id="d5f48-109">From the **Database** tab, select **Truncate**.</span></span>

4.  <span data-ttu-id="d5f48-110">На вкладке **Параметры** выберите **Усечение журнала на контрольной точки**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d5f48-110">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="d5f48-111">**Чтобы включить Truncate на контрольной точки в Microsoft SQL Server 7.0**</span><span class="sxs-lookup"><span data-stu-id="d5f48-111">**To enable Truncate on Checkpoint in Microsoft SQL Server 7.0**</span></span>

1.  <span data-ttu-id="d5f48-112">Запустите Microsoft SQL Server Enterprise Manager, откройте дерево для сервера и откройте дерево базы данных.</span><span class="sxs-lookup"><span data-stu-id="d5f48-112">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Databases tree.</span></span>

2.  <span data-ttu-id="d5f48-113">Щелкните правой кнопкой мыши имя базы данных, на котором этот компонент будет установлен и выберите команду **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="d5f48-113">Right-click the name of the database on which this feature will be enabled and choose **Properties**.</span></span>

3.  <span data-ttu-id="d5f48-114">На вкладке **Параметры** выберите **Усечение журнала на контрольной точки**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d5f48-114">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="d5f48-115">Дополнительные сведения о функции **Truncate на контрольной точки** документации Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d5f48-115">For more information about the **Truncate on Checkpoint** feature, see the Microsoft SQL Server documentation.</span></span>

