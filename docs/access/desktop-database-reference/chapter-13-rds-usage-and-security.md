---
title: Глава 13. Безопасность и использование RDS
TOCTitle: 'Chapter 13: RDS Usage and Security'
ms:assetid: 78add8bb-f01a-2efb-33f0-430deebefe8f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249495(v=office.15)
ms:contentKeyID: 48545756
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4250235d433572944d311611c909c060d2e69da9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876108"
---
# <a name="chapter-13-rds-usage-and-security"></a><span data-ttu-id="74630-102">Глава 13. Безопасность и использование RDS</span><span class="sxs-lookup"><span data-stu-id="74630-102">Chapter 13: RDS Usage and Security</span></span>


<span data-ttu-id="74630-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="74630-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="74630-104">Используйте сведения в этой главе, чтобы настроить сервер быстро и использовать служб удаленных рабочих СТОЛОВ.</span><span class="sxs-lookup"><span data-stu-id="74630-104">Use the information in this chapter to set up your server and use RDS quickly.</span></span> <span data-ttu-id="74630-105">В этой главе включает действия по настройке определенных, которые могут потребоваться при реализации служб удаленных рабочих СТОЛОВ, описываются некоторые основные отношения между служб удаленных рабочих СТОЛОВ и другие технологии, и помогает определить решения проблем, которые могут возникнуть при настройке Решение для служб удаленных рабочих СТОЛОВ.</span><span class="sxs-lookup"><span data-stu-id="74630-105">This chapter includes specific configuration steps that you might need to take when implementing RDS, describes some of the key relationships between RDS and other technologies, and helps identify solutions to problems that you might encounter when setting up an RDS solution.</span></span>

<span data-ttu-id="74630-106">В этом разделе содержатся следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="74630-106">This section contains information about:</span></span>

- [<span data-ttu-id="74630-107">Настройка RDS</span><span class="sxs-lookup"><span data-stu-id="74630-107">Configuring RDS</span></span>](configuring-rds.md)

- <span data-ttu-id="74630-108">[Предоставление гостевой привилегии на компьютере веб-сервера; Служб удаленных рабочих СТОЛОВ Гость привилегии \[ADO\]](granting-guest-privileges-to-a-web-server-computer;-rds-guest-privileges.md)</span><span class="sxs-lookup"><span data-stu-id="74630-108">[Granting Guest Privileges to a Web Server Computer; RDS guest privileges \[ADO\]](granting-guest-privileges-to-a-web-server-computer;-rds-guest-privileges.md)</span></span>

- [<span data-ttu-id="74630-109">Пометка бизнес-объектов как безопасных для написания скриптов</span><span class="sxs-lookup"><span data-stu-id="74630-109">Marking Business Objects as Safe for Scripting</span></span>](marking-business-objects-as-safe-for-scripting.md)

- [<span data-ttu-id="74630-110">Регистрация бизнес-объектов в клиенте для использования с DCOM</span><span class="sxs-lookup"><span data-stu-id="74630-110">Registering Business Objects on the Client for Use with DCOM</span></span>](registering-business-objects-on-the-client-for-use-with-dcom.md)

- [<span data-ttu-id="74630-111">Настройка формата маршалинга потоков DCOM</span><span class="sxs-lookup"><span data-stu-id="74630-111">Setting DCOM Stream Marshaling Format</span></span>](setting-dcom-stream-marshaling-format.md)

- [<span data-ttu-id="74630-112">Подготовка библиотеки DLL к работе в DCOM</span><span class="sxs-lookup"><span data-stu-id="74630-112">Enabling a DLL to Run on DCOM</span></span>](enabling-a-dll-to-run-on-dcom.md)

- [<span data-ttu-id="74630-113">Настройка виртуальных серверов в службах IIS</span><span class="sxs-lookup"><span data-stu-id="74630-113">Configuring Virtual Servers on IIS</span></span>](configuring-virtual-servers-on-iis.md)

- [<span data-ttu-id="74630-114">Указание числа потоков на процессор в службах IIS</span><span class="sxs-lookup"><span data-stu-id="74630-114">Specifying Threads Per Processor on IIS</span></span>](specifying-threads-per-processor-on-iis.md)

- [<span data-ttu-id="74630-115">Защита приложений RDS</span><span class="sxs-lookup"><span data-stu-id="74630-115">Securing RDS Applications</span></span>](securing-rds-applications.md)

- [<span data-ttu-id="74630-116">Настройка DataFactory для безопасного и нестрогого режимов</span><span class="sxs-lookup"><span data-stu-id="74630-116">Configuring DataFactory for Safe or Unrestricted Modes</span></span>](configuring-datafactory-for-safe-or-unrestricted-modes.md)

- [<span data-ttu-id="74630-117">Using Related Technologies with RDS (ADO)</span><span class="sxs-lookup"><span data-stu-id="74630-117">Using Related Technologies with RDS (ADO)</span></span>](using-related-technologies-with-rds.md)

- [<span data-ttu-id="74630-118">DataFactory Customization (ADO)</span><span class="sxs-lookup"><span data-stu-id="74630-118">DataFactory Customization (ADO)</span></span>](datafactory-customization.md)

- [<span data-ttu-id="74630-119">Troubleshooting RDS (ADO)</span><span class="sxs-lookup"><span data-stu-id="74630-119">Troubleshooting RDS (ADO)</span></span>](troubleshooting-rds.md)

