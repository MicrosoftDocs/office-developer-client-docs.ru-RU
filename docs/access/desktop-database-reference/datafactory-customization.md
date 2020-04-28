---
title: Настройка DataFactory
TOCTitle: DataFactory customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5fc1c284ee7aae77c4fb067ad57d50200119594
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294507"
---
# <a name="datafactory-customization"></a><span data-ttu-id="e426f-102">Настройка DataFactory</span><span class="sxs-lookup"><span data-stu-id="e426f-102">DataFactory customization</span></span>


<span data-ttu-id="e426f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e426f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e426f-104">Удаленная служба данных (RDS) позволяет легко осуществлять доступ к данным в трехуровневой клиент-серверной системе.</span><span class="sxs-lookup"><span data-stu-id="e426f-104">Remote Data Service (RDS) provides a way to easily perform data access in a three-tier client/server system.</span></span> <span data-ttu-id="e426f-105">Клиентский элемент управления данными определяет параметры подключения и командной строки для выполнения запроса на удаленном источнике данных, строки подключения и параметры объекта [Recordset](recordset-object-ado.md) для выполнения обновления.</span><span class="sxs-lookup"><span data-stu-id="e426f-105">A client data control specifies connection and command string parameters to perform a query on a remote data source, or connection string and [Recordset](recordset-object-ado.md) object parameters to perform an update.</span></span>

<span data-ttu-id="e426f-106">Параметры передаются в серверную программу, которая выполняет операцию доступа к данным на удаленном источнике данных.</span><span class="sxs-lookup"><span data-stu-id="e426f-106">The parameters are passed to a server program, which performs the data-access operation on the remote data source.</span></span> <span data-ttu-id="e426f-107">RDS предоставляет программу сервера по умолчанию с именем [рдссервер.](datafactory-object-rdsserver.md) DataObject.</span><span class="sxs-lookup"><span data-stu-id="e426f-107">RDS provides a default server program called the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span> <span data-ttu-id="e426f-108">Объект **рдссервер.** DataObject возвращает любой объект **Recordset** , созданный запросом к клиенту.</span><span class="sxs-lookup"><span data-stu-id="e426f-108">The **RDSServer.DataFactory** object returns any **Recordset** object produced by a query to the client.</span></span>

<span data-ttu-id="e426f-109">Тем не менее, **рдссервер. для фактов** ограничено выполнение запросов и обновлений.</span><span class="sxs-lookup"><span data-stu-id="e426f-109">However, the **RDSServer.DataFactory** is limited to performing queries and updates.</span></span> <span data-ttu-id="e426f-110">Она не может выполнять проверку или обработку для подключения или командных строк.</span><span class="sxs-lookup"><span data-stu-id="e426f-110">It cannot perform any validation or processing on the connection or command strings.</span></span>

<span data-ttu-id="e426f-111">С помощью ADO вы можете указать, что данные в **самом деле** работают совместно с другими типами серверных программ, которые называют *обработчиком*.</span><span class="sxs-lookup"><span data-stu-id="e426f-111">With ADO, you can specify that the **DataFactory** work in conjunction with another type of server program called a *handler*.</span></span> <span data-ttu-id="e426f-112">Обработчик может изменить клиентское соединение и строки команд, прежде чем они будут использоваться для доступа к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="e426f-112">The handler can modify client connection and command strings before they are used to access the data source.</span></span> <span data-ttu-id="e426f-113">Кроме того, обработчик может применять права доступа, которые определяют способность клиента считывать и записывать данные в источник данных.</span><span class="sxs-lookup"><span data-stu-id="e426f-113">In addition, the handler can enforce access rights, which govern the ability of the client to read and write data to the data source.</span></span>

<span data-ttu-id="e426f-114">Параметры, используемые обработчиком для изменения параметров клиента и прав доступа, указаны в разделах файла настройки.</span><span class="sxs-lookup"><span data-stu-id="e426f-114">The parameters the handler uses to modify client parameters and access rights are specified in sections of a customization file.</span></span>

<span data-ttu-id="e426f-115">В следующих разделах приводятся дополнительные сведения о настройке объекта **факты** данных:</span><span class="sxs-lookup"><span data-stu-id="e426f-115">See the following topics for more information about customizing the **DataFactory** object:</span></span>

- [<span data-ttu-id="e426f-116">Understanding the Customization File</span><span class="sxs-lookup"><span data-stu-id="e426f-116">Understanding the Customization File</span></span>](understanding-the-customization-file.md)
- [<span data-ttu-id="e426f-117">Раздел Connect в файле настройки</span><span class="sxs-lookup"><span data-stu-id="e426f-117">Customization File Connect section</span></span>](customization-file-connect-section.md)
- [<span data-ttu-id="e426f-118">Раздел SQL в файле настройки</span><span class="sxs-lookup"><span data-stu-id="e426f-118">Customization File SQL section</span></span>](customization-file-sql-section.md)
- [<span data-ttu-id="e426f-119">Раздел UserList в файле настройки</span><span class="sxs-lookup"><span data-stu-id="e426f-119">Customization File UserList section</span></span>](customization-file-userlist-section.md)
- [<span data-ttu-id="e426f-120">Раздел Logs в файле настройки</span><span class="sxs-lookup"><span data-stu-id="e426f-120">Customization File Logs section</span></span>](customization-file-logs-section.md)
- [<span data-ttu-id="e426f-121">Обязательные параметры клиента</span><span class="sxs-lookup"><span data-stu-id="e426f-121">Required client settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/required-client-settings)
- [<span data-ttu-id="e426f-122">Создание собственного пользовательского обработчика</span><span class="sxs-lookup"><span data-stu-id="e426f-122">Writing your own customized handler</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/writing-your-own-customized-handler)
