---
title: Настройка DataFactory для безопасного и нестрогого режимов
TOCTitle: Configuring DataFactory for Safe or Unrestricted Modes
ms:assetid: 1516068f-1b02-3236-f6a9-9fdeff098e52
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248915(v=office.15)
ms:contentKeyID: 48543400
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4f3658f3fdefeb87813319e4ed0313fe5c6032cf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882268"
---
# <a name="configuring-datafactory-for-safe-or-unrestricted-modes"></a><span data-ttu-id="9d345-102">Настройка DataFactory для безопасного и нестрогого режимов</span><span class="sxs-lookup"><span data-stu-id="9d345-102">Configuring DataFactory for Safe or Unrestricted Modes</span></span>


<span data-ttu-id="9d345-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d345-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9d345-104">По умолчанию ADO устанавливается вместе с «безопасный» [RDSServer.DataFactory](datafactory-object-rdsserver.md) конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9d345-104">By default, ADO is installed with a "safe" [RDSServer.DataFactory](datafactory-object-rdsserver.md) configuration.</span></span> <span data-ttu-id="9d345-105">Безопасного режима для компонентов сервера служб удаленных рабочих СТОЛОВ означает, что выполняются следующие условия:</span><span class="sxs-lookup"><span data-stu-id="9d345-105">Safe mode for RDS Server components means that the following are true:</span></span>

1.  <span data-ttu-id="9d345-106">Обработчик является обязательным с RDSServer.DataFactory, (это является предусмотренные раздела реестра).</span><span class="sxs-lookup"><span data-stu-id="9d345-106">Handler is required with the RDSServer.DataFactory (this is mandated by a registry key setting).</span></span>

2.  <span data-ttu-id="9d345-107">Обработчик по умолчанию, msdfmap.handler, зарегистрированных, присутствует в списке безопасных обработчика и помеченные как обработчик по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9d345-107">The default handler, msdfmap.handler, is registered, present in the safe-handler list, and marked as the default handler.</span></span>

3.  <span data-ttu-id="9d345-108">Файл Msdfmap.ini устанавливается в каталоге Windows.</span><span class="sxs-lookup"><span data-stu-id="9d345-108">Msdfmap.ini file is installed in the Windows directory.</span></span> <span data-ttu-id="9d345-109">По мере необходимости, перед использованием служб удаленных рабочих СТОЛОВ в режим трехуровневой необходимо настроить этот файл.</span><span class="sxs-lookup"><span data-stu-id="9d345-109">You must configure this file according to your needs, before using RDS in three-tier mode.</span></span>

<span data-ttu-id="9d345-110">При необходимости можно настроить неограниченный установки **DataFactory** .</span><span class="sxs-lookup"><span data-stu-id="9d345-110">Optionally, you can configure an unrestricted **DataFactory** installation.</span></span> <span data-ttu-id="9d345-111">**DataFactory** может использоваться напрямую без пользовательский обработчик.</span><span class="sxs-lookup"><span data-stu-id="9d345-111">**DataFactory** can be used directly without the custom handler.</span></span> <span data-ttu-id="9d345-112">Пользователи по-прежнему могут использовать пользовательский обработчик путем изменения строки подключения, но не требуется.</span><span class="sxs-lookup"><span data-stu-id="9d345-112">Users can still use a custom handler by modifying the connection strings, but it is not required.</span></span> <span data-ttu-id="9d345-113">Дополнительные сведения о влиянии с помощью объекта **RDSServer.DataFactory** [Обеспечение безопасности приложений служб удаленных рабочих СТОЛОВ](securing-rds-applications.md)см.</span><span class="sxs-lookup"><span data-stu-id="9d345-113">For more information about the implications of using the **RDSServer.DataFactory** object, see [Securing RDS Applications](securing-rds-applications.md).</span></span>

<span data-ttu-id="9d345-114">Настройка записей реестра обработчик для настройки безопасных было предоставлено handsafe.reg файла реестра.</span><span class="sxs-lookup"><span data-stu-id="9d345-114">The registry file handsafe.reg has been provided to set up the handler registry entries for a safe configuration.</span></span> <span data-ttu-id="9d345-115">Чтобы запустить в безопасном режиме, запустите handsafe.reg. Настройка записей реестра обработчик для неограниченный конфигурации было предоставлено handunsf.reg файла реестра.</span><span class="sxs-lookup"><span data-stu-id="9d345-115">To run in safe mode, run handsafe.reg. The registry file handunsf.reg has been provided to set up the handler registry entries for an unrestricted configuration.</span></span> <span data-ttu-id="9d345-116">Чтобы запустить в режиме без ограничений, запустите handunsf.reg.</span><span class="sxs-lookup"><span data-stu-id="9d345-116">To run in unrestricted mode, run handunsf.reg.</span></span>

<span data-ttu-id="9d345-117">После выполнения handsafe.reg или handunsf.reg, необходимо остановить и перезапустить службу публикации Интернета на веб-сервере, введя следующие команды в командной строке: «NET STOP W3SVC» и «W3SVC ЗАПУСТИТЕ NET».</span><span class="sxs-lookup"><span data-stu-id="9d345-117">After running either handsafe.reg or handunsf.reg, you must stop and restart the World Wide Web Publishing Service on the web server by typing the following commands in a command window: "NET STOP W3SVC" and "NET START W3SVC".</span></span>

<span data-ttu-id="9d345-118">Дополнительные сведения об использовании компонента обработчика настройки из служб удаленных рабочих СТОЛОВ в статье технические с помощью компонента обработчика настройки в 2.1 служб удаленных рабочих СТОЛОВ.</span><span class="sxs-lookup"><span data-stu-id="9d345-118">For more information about using the customization handler feature of RDS, see the technical article Using the Customization Handler Feature in RDS 2.1.</span></span>

