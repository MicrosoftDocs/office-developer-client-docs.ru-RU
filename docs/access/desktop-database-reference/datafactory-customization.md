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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700026"
---
# <a name="datafactory-customization"></a><span data-ttu-id="b7d90-102">Настройка DataFactory</span><span class="sxs-lookup"><span data-stu-id="b7d90-102">DataFactory customization</span></span>


<span data-ttu-id="b7d90-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7d90-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7d90-104">Службы удаленных данных (RDS) позволяет легко осуществлять доступ к данным в системе с трехуровневой клиента и сервера.</span><span class="sxs-lookup"><span data-stu-id="b7d90-104">Remote Data Service (RDS) provides a way to easily perform data access in a three-tier client/server system.</span></span> <span data-ttu-id="b7d90-105">Данные клиентского элемента управления определяет подключение и параметры командной строки для выполнения запросов к удаленному источнику данных, или строку подключения и параметры объекта [набора записей](recordset-object-ado.md) для выполнения обновления.</span><span class="sxs-lookup"><span data-stu-id="b7d90-105">A client data control specifies connection and command string parameters to perform a query on a remote data source, or connection string and [Recordset](recordset-object-ado.md) object parameters to perform an update.</span></span>

<span data-ttu-id="b7d90-106">Параметры передаются в программу сервера, который выполняет операцию доступа к данным к удаленному источнику данных.</span><span class="sxs-lookup"><span data-stu-id="b7d90-106">The parameters are passed to a server program, which performs the data-access operation on the remote data source.</span></span> <span data-ttu-id="b7d90-107">Служб удаленных рабочих СТОЛОВ предоставляет программы сервера по умолчанию, называется объектом [RDSServer.DataFactory](datafactory-object-rdsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="b7d90-107">RDS provides a default server program called the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span> <span data-ttu-id="b7d90-108">Объект **RDSServer.DataFactory** возвращает любого объекта **набора записей** , создаваемых в запрос для клиента.</span><span class="sxs-lookup"><span data-stu-id="b7d90-108">The **RDSServer.DataFactory** object returns any **Recordset** object produced by a query to the client.</span></span>

<span data-ttu-id="b7d90-109">Тем не менее, **RDSServer.DataFactory** ограничено для выполнения запросов и обновлений.</span><span class="sxs-lookup"><span data-stu-id="b7d90-109">However, the **RDSServer.DataFactory** is limited to performing queries and updates.</span></span> <span data-ttu-id="b7d90-110">Он не может выполнять любые проверки или обработки на подключение или командной строки.</span><span class="sxs-lookup"><span data-stu-id="b7d90-110">It cannot perform any validation or processing on the connection or command strings.</span></span>

<span data-ttu-id="b7d90-111">С помощью ADO можно указать, что рабочий **DataFactory** совместно с другого типа программы сервера вызваны *обработчика*.</span><span class="sxs-lookup"><span data-stu-id="b7d90-111">With ADO, you can specify that the **DataFactory** work in conjunction with another type of server program called a *handler*.</span></span> <span data-ttu-id="b7d90-112">Обработчик можно изменить подключение к клиенту и командной строки перед их использования для доступа к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="b7d90-112">The handler can modify client connection and command strings before they are used to access the data source.</span></span> <span data-ttu-id="b7d90-113">Кроме того обработчик может задать права доступа, которые управляют возможности клиента для чтения и записи данных в источник данных.</span><span class="sxs-lookup"><span data-stu-id="b7d90-113">In addition, the handler can enforce access rights, which govern the ability of the client to read and write data to the data source.</span></span>

<span data-ttu-id="b7d90-114">В разделах файл настройки заданы параметры, которые обработчик использует, чтобы изменить параметры клиента и прав доступа.</span><span class="sxs-lookup"><span data-stu-id="b7d90-114">The parameters the handler uses to modify client parameters and access rights are specified in sections of a customization file.</span></span>

<span data-ttu-id="b7d90-115">В следующих разделах Дополнительные сведения о настройке **DataFactory** объектов:</span><span class="sxs-lookup"><span data-stu-id="b7d90-115">See the following topics for more information about customizing the **DataFactory** object:</span></span>

- [<span data-ttu-id="b7d90-116">Общие сведения о файле настройки</span><span class="sxs-lookup"><span data-stu-id="b7d90-116">Understanding the Customization File</span></span>](understanding-the-customization-file.md)
- [<span data-ttu-id="b7d90-117">Раздел Connect в файле настройки</span><span class="sxs-lookup"><span data-stu-id="b7d90-117">Customization File Connect section</span></span>](customization-file-connect-section.md)
- [<span data-ttu-id="b7d90-118">Раздел SQL в файле настройки</span><span class="sxs-lookup"><span data-stu-id="b7d90-118">Customization File SQL section</span></span>](customization-file-sql-section.md)
- [<span data-ttu-id="b7d90-119">Раздел UserList в файле настройки</span><span class="sxs-lookup"><span data-stu-id="b7d90-119">Customization File UserList section</span></span>](customization-file-userlist-section.md)
- [<span data-ttu-id="b7d90-120">Раздел Logs в файле настройки</span><span class="sxs-lookup"><span data-stu-id="b7d90-120">Customization File Logs section</span></span>](customization-file-logs-section.md)
- [<span data-ttu-id="b7d90-121">Обязательные параметры клиента</span><span class="sxs-lookup"><span data-stu-id="b7d90-121">Required client settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/required-client-settings)
- [<span data-ttu-id="b7d90-122">Создание настраиваемого обработчика</span><span class="sxs-lookup"><span data-stu-id="b7d90-122">Writing your own customized handler</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/writing-your-own-customized-handler)
