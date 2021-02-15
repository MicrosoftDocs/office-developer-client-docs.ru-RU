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
# <a name="datafactory-customization"></a><span data-ttu-id="c1bd0-102">Настройка DataFactory</span><span class="sxs-lookup"><span data-stu-id="c1bd0-102">DataFactory customization</span></span>


<span data-ttu-id="c1bd0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c1bd0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c1bd0-104">Удаленная служба данных (RDS) позволяет легко выполнять доступ к данным в трехуровневой клиентской или серверной системе.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-104">Remote Data Service (RDS) provides a way to easily perform data access in a three-tier client/server system.</span></span> <span data-ttu-id="c1bd0-105">Клиентский объект управления данными указывает параметры подключения и строки команды для выполнения запроса к удаленному источнику данных, строку подключения и параметры объекта [Recordset](recordset-object-ado.md) для выполнения обновления.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-105">A client data control specifies connection and command string parameters to perform a query on a remote data source, or connection string and [Recordset](recordset-object-ado.md) object parameters to perform an update.</span></span>

<span data-ttu-id="c1bd0-106">Параметры передаются серверной программе, которая выполняет операцию доступа к данным в удаленном источнике данных.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-106">The parameters are passed to a server program, which performs the data-access operation on the remote data source.</span></span> <span data-ttu-id="c1bd0-107">RDS предоставляет серверную программу по умолчанию, которая называется [объектом RDSServer.DataFactory.](datafactory-object-rdsserver.md)</span><span class="sxs-lookup"><span data-stu-id="c1bd0-107">RDS provides a default server program called the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span> <span data-ttu-id="c1bd0-108">Объект **RDSServer.DataFactory** возвращает клиенту объект **Recordset,** полученный запросом.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-108">The **RDSServer.DataFactory** object returns any **Recordset** object produced by a query to the client.</span></span>

<span data-ttu-id="c1bd0-109">Однако **RDSServer.DataFactory** ограничивается выполнением запросов и обновлений.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-109">However, the **RDSServer.DataFactory** is limited to performing queries and updates.</span></span> <span data-ttu-id="c1bd0-110">Он не может выполнять проверку или обработку для подключения или строк команд.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-110">It cannot perform any validation or processing on the connection or command strings.</span></span>

<span data-ttu-id="c1bd0-111">С помощью ADO можно указать, что **DataFactory** работает в сочетании с другим типом серверной программы, который называется *обработчиком.*</span><span class="sxs-lookup"><span data-stu-id="c1bd0-111">With ADO, you can specify that the **DataFactory** work in conjunction with another type of server program called a *handler*.</span></span> <span data-ttu-id="c1bd0-112">Обработник может изменять клиентские подключения и строки команд, прежде чем они будут использоваться для доступа к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-112">The handler can modify client connection and command strings before they are used to access the data source.</span></span> <span data-ttu-id="c1bd0-113">Кроме того, обработник может применять права доступа, которые управляют возможностью клиента читать и записывать данные в источник данных.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-113">In addition, the handler can enforce access rights, which govern the ability of the client to read and write data to the data source.</span></span>

<span data-ttu-id="c1bd0-114">Параметры, которые обработок использует для изменения параметров клиента и прав доступа, заданы в разделах файла настройки.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-114">The parameters the handler uses to modify client parameters and access rights are specified in sections of a customization file.</span></span>

<span data-ttu-id="c1bd0-115">Дополнительные сведения о настройке объекта **DataFactory** см. в следующих темах:</span><span class="sxs-lookup"><span data-stu-id="c1bd0-115">See the following topics for more information about customizing the **DataFactory** object:</span></span>

- [<span data-ttu-id="c1bd0-116">Understanding the Customization File</span><span class="sxs-lookup"><span data-stu-id="c1bd0-116">Understanding the Customization File</span></span>](understanding-the-customization-file.md)
- [<span data-ttu-id="c1bd0-117">Раздел Connect в файле настройки</span><span class="sxs-lookup"><span data-stu-id="c1bd0-117">Customization File Connect section</span></span>](customization-file-connect-section.md)
- [<span data-ttu-id="c1bd0-118">Раздел SQL в файле настройки</span><span class="sxs-lookup"><span data-stu-id="c1bd0-118">Customization File SQL section</span></span>](customization-file-sql-section.md)
- [<span data-ttu-id="c1bd0-119">Раздел UserList в файле настройки</span><span class="sxs-lookup"><span data-stu-id="c1bd0-119">Customization File UserList section</span></span>](customization-file-userlist-section.md)
- [<span data-ttu-id="c1bd0-120">Раздел Logs в файле настройки</span><span class="sxs-lookup"><span data-stu-id="c1bd0-120">Customization File Logs section</span></span>](customization-file-logs-section.md)
- [<span data-ttu-id="c1bd0-121">Обязательные параметры клиента</span><span class="sxs-lookup"><span data-stu-id="c1bd0-121">Required client settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/required-client-settings)
- [<span data-ttu-id="c1bd0-122">Написание собственного настраиваемой обработки</span><span class="sxs-lookup"><span data-stu-id="c1bd0-122">Writing your own customized handler</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/writing-your-own-customized-handler)
