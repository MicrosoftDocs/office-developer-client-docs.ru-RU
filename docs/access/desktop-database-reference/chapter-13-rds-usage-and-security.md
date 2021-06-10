---
title: Глава 13. Безопасность и использование RDS
TOCTitle: 'Chapter 13: RDS usage and security'
ms:assetid: 78add8bb-f01a-2efb-33f0-430deebefe8f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249495(v=office.15)
ms:contentKeyID: 48545756
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4c0753a53a2001a6c5c96ae2ceb801ee6eb75a5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296474"
---
# <a name="chapter-13-rds-usage-and-security"></a><span data-ttu-id="2537e-102">Глава 13. Безопасность и использование RDS</span><span class="sxs-lookup"><span data-stu-id="2537e-102">Chapter 13: RDS usage and security</span></span>

<span data-ttu-id="2537e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2537e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2537e-104">Используйте сведения в этой главе, чтобы настроить сервер и быстро использовать RDS.</span><span class="sxs-lookup"><span data-stu-id="2537e-104">Use the information in this chapter to set up your server and use RDS quickly.</span></span> <span data-ttu-id="2537e-105">В этой главе содержатся конкретные действия по настройке, которые необходимо предпринять при реализации RDS, описываются некоторые ключевые связи между RDS и другими технологиями, а также определяются решения проблем, с которыми вы можете столкнуться при настройке решения RDS.</span><span class="sxs-lookup"><span data-stu-id="2537e-105">This chapter includes specific configuration steps that you might need to take when implementing RDS, describes some of the key relationships between RDS and other technologies, and helps identify solutions to problems that you might encounter when setting up an RDS solution.</span></span>

<span data-ttu-id="2537e-106">В этом разделе содержатся сведения о:</span><span class="sxs-lookup"><span data-stu-id="2537e-106">This section contains information about:</span></span>

- [<span data-ttu-id="2537e-107">Настройка DataFactory для безопасного или неограниченного режима</span><span class="sxs-lookup"><span data-stu-id="2537e-107">Configuring DataFactory for safe or unrestricted modes</span></span>](configuring-datafactory-for-safe-or-unrestricted-modes.md)
- [<span data-ttu-id="2537e-108">Configuring RDS</span><span class="sxs-lookup"><span data-stu-id="2537e-108">Configuring RDS</span></span>](configuring-rds.md)
- [<span data-ttu-id="2537e-109">Настройка виртуальных серверов в IIS</span><span class="sxs-lookup"><span data-stu-id="2537e-109">Configuring virtual servers on IIS</span></span>](configuring-virtual-servers-on-iis.md)
- [<span data-ttu-id="2537e-110">Настройка DataFactory (ADO)</span><span class="sxs-lookup"><span data-stu-id="2537e-110">DataFactory customization (ADO)</span></span>](datafactory-customization.md)
- [<span data-ttu-id="2537e-111">Подготовка библиотеки DLL к работе в DCOM</span><span class="sxs-lookup"><span data-stu-id="2537e-111">Enabling a DLL to run on DCOM</span></span>](enabling-a-dll-to-run-on-dcom.md)
- <span data-ttu-id="2537e-112">[Предоставление гостевых привилегий компьютеру веб-сервера; Гостевых привилегий \[ RDS ADO\]](granting-guest-privileges-to-a-web-server-computer;-rds-guest-privileges.md)</span><span class="sxs-lookup"><span data-stu-id="2537e-112">[Granting guest privileges to a web server computer; RDS guest privileges \[ADO\]](granting-guest-privileges-to-a-web-server-computer;-rds-guest-privileges.md)</span></span>
- [<span data-ttu-id="2537e-113">Пометка бизнес-объектов как безопасных для написания скриптов</span><span class="sxs-lookup"><span data-stu-id="2537e-113">Marking business objects as safe for scripting</span></span>](marking-business-objects-as-safe-for-scripting.md)
- [<span data-ttu-id="2537e-114">Регистрация бизнес-объектов в клиенте для использования с DCOM</span><span class="sxs-lookup"><span data-stu-id="2537e-114">Registering business objects on the client for use with DCOM</span></span>](registering-business-objects-on-the-client-for-use-with-dcom.md)
- [<span data-ttu-id="2537e-115">Защита приложений RDS</span><span class="sxs-lookup"><span data-stu-id="2537e-115">Securing RDS applications</span></span>](securing-rds-applications.md)
- [<span data-ttu-id="2537e-116">Настройка формата маршалинга потоков DCOM</span><span class="sxs-lookup"><span data-stu-id="2537e-116">Setting DCOM stream marshaling format</span></span>](setting-dcom-stream-marshaling-format.md)
- [<span data-ttu-id="2537e-117">Указание числа потоков на процессор в IIS</span><span class="sxs-lookup"><span data-stu-id="2537e-117">Specifying threads per processor on IIS</span></span>](specifying-threads-per-processor-on-iis.md)
- [<span data-ttu-id="2537e-118">Troubleshooting RDS (ADO)</span><span class="sxs-lookup"><span data-stu-id="2537e-118">Troubleshooting RDS (ADO)</span></span>](troubleshooting-rds.md)
- [<span data-ttu-id="2537e-119">Использование связанных технологий с помощью RDS (ADO)</span><span class="sxs-lookup"><span data-stu-id="2537e-119">Using related technologies with RDS (ADO)</span></span>](using-related-technologies-with-rds.md)














