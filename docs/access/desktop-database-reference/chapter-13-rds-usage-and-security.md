---
title: 'Глава 13: Об использовании служб удаленных рабочих СТОЛОВ и безопасности'
TOCTitle: 'Chapter 13: RDS usage and security'
ms:assetid: 78add8bb-f01a-2efb-33f0-430deebefe8f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249495(v=office.15)
ms:contentKeyID: 48545756
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 21f1484850a91d1fbdbe687f171e8ae9dfe4a5cd
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936471"
---
# <a name="chapter-13-rds-usage-and-security"></a><span data-ttu-id="fc6ec-102">Глава 13: Об использовании служб удаленных рабочих СТОЛОВ и безопасности</span><span class="sxs-lookup"><span data-stu-id="fc6ec-102">Chapter 13: RDS usage and security</span></span>

<span data-ttu-id="fc6ec-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc6ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fc6ec-104">Используйте сведения в этой главе, чтобы настроить сервер быстро и использовать служб удаленных рабочих СТОЛОВ.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-104">Use the information in this chapter to set up your server and use RDS quickly.</span></span> <span data-ttu-id="fc6ec-105">В этой главе включает действия по настройке определенных, которые могут потребоваться при реализации служб удаленных рабочих СТОЛОВ, описываются некоторые основные отношения между служб удаленных рабочих СТОЛОВ и другие технологии, и помогает определить решения проблем, которые могут возникнуть при настройке Решение для служб удаленных рабочих СТОЛОВ.</span><span class="sxs-lookup"><span data-stu-id="fc6ec-105">This chapter includes specific configuration steps that you might need to take when implementing RDS, describes some of the key relationships between RDS and other technologies, and helps identify solutions to problems that you might encounter when setting up an RDS solution.</span></span>

<span data-ttu-id="fc6ec-106">В этом разделе содержатся следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="fc6ec-106">This section contains information about:</span></span>

- [<span data-ttu-id="fc6ec-107">Настройка DataFactory для режимов безопасных или без ограничений</span><span class="sxs-lookup"><span data-stu-id="fc6ec-107">Configuring DataFactory for safe or unrestricted modes</span></span>](configuring-datafactory-for-safe-or-unrestricted-modes.md)
- [<span data-ttu-id="fc6ec-108">Настройка RDS</span><span class="sxs-lookup"><span data-stu-id="fc6ec-108">Configuring RDS</span></span>](configuring-rds.md)
- [<span data-ttu-id="fc6ec-109">Настройка виртуальных серверов в IIS</span><span class="sxs-lookup"><span data-stu-id="fc6ec-109">Configuring virtual servers on IIS</span></span>](configuring-virtual-servers-on-iis.md)
- [<span data-ttu-id="fc6ec-110">Настройка DataFactory (ADO)</span><span class="sxs-lookup"><span data-stu-id="fc6ec-110">DataFactory customization (ADO)</span></span>](datafactory-customization.md)
- [<span data-ttu-id="fc6ec-111">Включение библиотеки DLL для запуска на DCOM</span><span class="sxs-lookup"><span data-stu-id="fc6ec-111">Enabling a DLL to run on DCOM</span></span>](enabling-a-dll-to-run-on-dcom.md)
- <span data-ttu-id="fc6ec-112">[Предоставление права гостевой на компьютере веб-сервера; Служб удаленных рабочих СТОЛОВ Гость привилегии \[ADO\]](granting-guest-privileges-to-a-web-server-computer;-rds-guest-privileges.md)</span><span class="sxs-lookup"><span data-stu-id="fc6ec-112">[Granting guest privileges to a web server computer; RDS guest privileges \[ADO\]](granting-guest-privileges-to-a-web-server-computer;-rds-guest-privileges.md)</span></span>
- [<span data-ttu-id="fc6ec-113">Пометка бизнес-объекты как безопасные для скриптов</span><span class="sxs-lookup"><span data-stu-id="fc6ec-113">Marking business objects as safe for scripting</span></span>](marking-business-objects-as-safe-for-scripting.md)
- [<span data-ttu-id="fc6ec-114">Регистрация бизнес-объекты на стороне клиента для использования с DCOM</span><span class="sxs-lookup"><span data-stu-id="fc6ec-114">Registering business objects on the client for use with DCOM</span></span>](registering-business-objects-on-the-client-for-use-with-dcom.md)
- [<span data-ttu-id="fc6ec-115">Обеспечение безопасности приложений служб удаленных рабочих СТОЛОВ</span><span class="sxs-lookup"><span data-stu-id="fc6ec-115">Securing RDS applications</span></span>](securing-rds-applications.md)
- [<span data-ttu-id="fc6ec-116">Установка DCOM потока маршалинга формата</span><span class="sxs-lookup"><span data-stu-id="fc6ec-116">Setting DCOM stream marshaling format</span></span>](setting-dcom-stream-marshaling-format.md)
- [<span data-ttu-id="fc6ec-117">Указание потоков процессора на сервере IIS</span><span class="sxs-lookup"><span data-stu-id="fc6ec-117">Specifying threads per processor on IIS</span></span>](specifying-threads-per-processor-on-iis.md)
- [<span data-ttu-id="fc6ec-118">Troubleshooting RDS (ADO)</span><span class="sxs-lookup"><span data-stu-id="fc6ec-118">Troubleshooting RDS (ADO)</span></span>](troubleshooting-rds.md)
- [<span data-ttu-id="fc6ec-119">С помощью связанных технологиях с помощью служб удаленных рабочих СТОЛОВ (ADO)</span><span class="sxs-lookup"><span data-stu-id="fc6ec-119">Using related technologies with RDS (ADO)</span></span>](using-related-technologies-with-rds.md)














