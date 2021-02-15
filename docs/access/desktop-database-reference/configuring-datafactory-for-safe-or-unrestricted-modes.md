---
title: Configuring DataFactory for Safe or Unrestricted Modes
TOCTitle: Configuring DataFactory for Safe or Unrestricted Modes
ms:assetid: 1516068f-1b02-3236-f6a9-9fdeff098e52
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248915(v=office.15)
ms:contentKeyID: 48543400
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4313d48359499eaf249a68eb97408c8ed4ecb88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295998"
---
# <a name="configuring-datafactory-for-safe-or-unrestricted-modes"></a><span data-ttu-id="d7b9c-102">Configuring DataFactory for Safe or Unrestricted Modes</span><span class="sxs-lookup"><span data-stu-id="d7b9c-102">Configuring DataFactory for Safe or Unrestricted Modes</span></span>


<span data-ttu-id="d7b9c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7b9c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7b9c-104">По умолчанию ADO устанавливается с "безопасной" [конфигурацией RDSServer.DataFactory.](datafactory-object-rdsserver.md)</span><span class="sxs-lookup"><span data-stu-id="d7b9c-104">By default, ADO is installed with a "safe" [RDSServer.DataFactory](datafactory-object-rdsserver.md) configuration.</span></span> <span data-ttu-id="d7b9c-105">Безопасный режим для компонентов сервера RDS означает, что истинны следующие:</span><span class="sxs-lookup"><span data-stu-id="d7b9c-105">Safe mode for RDS Server components means that the following are true:</span></span>

1.  <span data-ttu-id="d7b9c-106">Обработчик необходим для RDSServer.DataFactory (это задано параметром ключа реестра).</span><span class="sxs-lookup"><span data-stu-id="d7b9c-106">Handler is required with the RDSServer.DataFactory (this is mandated by a registry key setting).</span></span>

2.  <span data-ttu-id="d7b9c-107">Обработтель по умолчанию, msdfmap.handler, зарегистрирован, присутствует в списке безопасных обработщиков и помечен как обработтель по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d7b9c-107">The default handler, msdfmap.handler, is registered, present in the safe-handler list, and marked as the default handler.</span></span>

3.  <span data-ttu-id="d7b9c-108">Msdfmap.ini файл установлен в каталоге Windows.</span><span class="sxs-lookup"><span data-stu-id="d7b9c-108">Msdfmap.ini file is installed in the Windows directory.</span></span> <span data-ttu-id="d7b9c-109">Этот файл необходимо настроить в соответствии с потребностями, прежде чем использовать RDS в трехуровневом режиме.</span><span class="sxs-lookup"><span data-stu-id="d7b9c-109">You must configure this file according to your needs, before using RDS in three-tier mode.</span></span>

<span data-ttu-id="d7b9c-110">При желании можно настроить неоконфигурированную **установку DataFactory.**</span><span class="sxs-lookup"><span data-stu-id="d7b9c-110">Optionally, you can configure an unrestricted **DataFactory** installation.</span></span> <span data-ttu-id="d7b9c-111">**DataFactory** можно использовать напрямую без настраиваемого обработчика.</span><span class="sxs-lookup"><span data-stu-id="d7b9c-111">**DataFactory** can be used directly without the custom handler.</span></span> <span data-ttu-id="d7b9c-112">Пользователи по-прежнему могут использовать настраиваемый обработок, изменяя строки подключения, но это не требуется.</span><span class="sxs-lookup"><span data-stu-id="d7b9c-112">Users can still use a custom handler by modifying the connection strings, but it is not required.</span></span> <span data-ttu-id="d7b9c-113">Дополнительные сведения о последствиях использования объекта **RDSServer.DataFactory** см. в подраздеке "Защита приложений [RDS".](securing-rds-applications.md)</span><span class="sxs-lookup"><span data-stu-id="d7b9c-113">For more information about the implications of using the **RDSServer.DataFactory** object, see [Securing RDS Applications](securing-rds-applications.md).</span></span>

<span data-ttu-id="d7b9c-114">Файл реестра handsafe.reg был предоставлен для настройки записей реестра обработок для безопасной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d7b9c-114">The registry file handsafe.reg has been provided to set up the handler registry entries for a safe configuration.</span></span> <span data-ttu-id="d7b9c-115">Чтобы запустить в безопасном режиме, запустите handsafe.reg. Файл реестра handunsf.reg был предоставлен для настройки записей реестра обработителя для неограниченной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d7b9c-115">To run in safe mode, run handsafe.reg. The registry file handunsf.reg has been provided to set up the handler registry entries for an unrestricted configuration.</span></span> <span data-ttu-id="d7b9c-116">Чтобы работать в неограниченном режиме, запустите handunsf.reg.</span><span class="sxs-lookup"><span data-stu-id="d7b9c-116">To run in unrestricted mode, run handunsf.reg.</span></span>

<span data-ttu-id="d7b9c-117">После запуска handsafe.reg или handunsf.reg необходимо остановить и перезапустить службу веб-публикации на веб-сервере, введя в командном окне следующие команды: "NET STOP W3SVC" и "NET START W3SVC".</span><span class="sxs-lookup"><span data-stu-id="d7b9c-117">After running either handsafe.reg or handunsf.reg, you must stop and restart the World Wide Web Publishing Service on the web server by typing the following commands in a command window: "NET STOP W3SVC" and "NET START W3SVC".</span></span>

<span data-ttu-id="d7b9c-118">Дополнительные сведения об использовании функции обработки настроек RDS см. в технической статье "Использование функции обработки настроек в RDS 2.1".</span><span class="sxs-lookup"><span data-stu-id="d7b9c-118">For more information about using the customization handler feature of RDS, see the technical article Using the Customization Handler Feature in RDS 2.1.</span></span>

