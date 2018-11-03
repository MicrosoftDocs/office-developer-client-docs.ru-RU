---
title: Настройка DataFactory
TOCTitle: DataFactory customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9de748b85e4bf6076c37f49e9d9bc7ff3b0bfe62
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947575"
---
# <a name="datafactory-customization"></a><span data-ttu-id="f5f02-102">Настройка DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5f02-102">DataFactory customization</span></span>


<span data-ttu-id="f5f02-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f5f02-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f5f02-104">Службы удаленных данных (RDS) позволяет легко осуществлять доступ к данным в системе с трехуровневой клиента и сервера.</span><span class="sxs-lookup"><span data-stu-id="f5f02-104">Remote Data Service (RDS) provides a way to easily perform data access in a three-tier client/server system.</span></span> <span data-ttu-id="f5f02-105">Данные клиентского элемента управления определяет подключение и параметры командной строки для выполнения запросов к удаленному источнику данных, или строку подключения и параметры объекта [набора записей](recordset-object-ado.md) для выполнения обновления.</span><span class="sxs-lookup"><span data-stu-id="f5f02-105">A client data control specifies connection and command string parameters to perform a query on a remote data source, or connection string and [Recordset](recordset-object-ado.md) object parameters to perform an update.</span></span>

<span data-ttu-id="f5f02-106">Параметры передаются в программу сервера, который выполняет операцию доступа к данным к удаленному источнику данных.</span><span class="sxs-lookup"><span data-stu-id="f5f02-106">The parameters are passed to a server program, which performs the data-access operation on the remote data source.</span></span> <span data-ttu-id="f5f02-107">Служб удаленных рабочих СТОЛОВ предоставляет программы сервера по умолчанию, называется объектом [RDSServer.DataFactory](datafactory-object-rdsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="f5f02-107">RDS provides a default server program called the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span> <span data-ttu-id="f5f02-108">Объект **RDSServer.DataFactory** возвращает любого объекта **набора записей** , создаваемых в запрос для клиента.</span><span class="sxs-lookup"><span data-stu-id="f5f02-108">The **RDSServer.DataFactory** object returns any **Recordset** object produced by a query to the client.</span></span>

<span data-ttu-id="f5f02-109">Тем не менее, **RDSServer.DataFactory** ограничено для выполнения запросов и обновлений.</span><span class="sxs-lookup"><span data-stu-id="f5f02-109">However, the **RDSServer.DataFactory** is limited to performing queries and updates.</span></span> <span data-ttu-id="f5f02-110">Он не может выполнять любые проверки или обработки на подключение или командной строки.</span><span class="sxs-lookup"><span data-stu-id="f5f02-110">It cannot perform any validation or processing on the connection or command strings.</span></span>

<span data-ttu-id="f5f02-111">С помощью ADO можно указать, что рабочий **DataFactory** совместно с другого типа программы сервера вызваны *обработчика*.</span><span class="sxs-lookup"><span data-stu-id="f5f02-111">With ADO, you can specify that the **DataFactory** work in conjunction with another type of server program called a *handler*.</span></span> <span data-ttu-id="f5f02-112">Обработчик можно изменить подключение к клиенту и командной строки перед их использования для доступа к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="f5f02-112">The handler can modify client connection and command strings before they are used to access the data source.</span></span> <span data-ttu-id="f5f02-113">Кроме того обработчик может задать права доступа, которые управляют возможности клиента для чтения и записи данных в источник данных.</span><span class="sxs-lookup"><span data-stu-id="f5f02-113">In addition, the handler can enforce access rights, which govern the ability of the client to read and write data to the data source.</span></span>

<span data-ttu-id="f5f02-114">В разделах файл настройки заданы параметры, которые обработчик использует, чтобы изменить параметры клиента и прав доступа.</span><span class="sxs-lookup"><span data-stu-id="f5f02-114">The parameters the handler uses to modify client parameters and access rights are specified in sections of a customization file.</span></span>

<span data-ttu-id="f5f02-115">В следующих разделах Дополнительные сведения о настройке **DataFactory** объектов:</span><span class="sxs-lookup"><span data-stu-id="f5f02-115">See the following topics for more information about customizing the **DataFactory** object:</span></span>

- [<span data-ttu-id="f5f02-116">Общие сведения о файле настройки</span><span class="sxs-lookup"><span data-stu-id="f5f02-116">Understanding the Customization File</span></span>](understanding-the-customization-file.md)
- [<span data-ttu-id="f5f02-117">Раздел подключение файла настройки</span><span class="sxs-lookup"><span data-stu-id="f5f02-117">Customization File Connect section</span></span>](customization-file-connect-section.md)
- [<span data-ttu-id="f5f02-118">Раздел настройки файла SQL</span><span class="sxs-lookup"><span data-stu-id="f5f02-118">Customization File SQL section</span></span>](customization-file-sql-section.md)
- [<span data-ttu-id="f5f02-119">Раздел UserList файл настройки</span><span class="sxs-lookup"><span data-stu-id="f5f02-119">Customization File UserList section</span></span>](customization-file-userlist-section.md)
- [<span data-ttu-id="f5f02-120">Раздел настройки файлов журналов</span><span class="sxs-lookup"><span data-stu-id="f5f02-120">Customization File Logs section</span></span>](customization-file-logs-section.md)
- [<span data-ttu-id="f5f02-121">Параметры необходимые клиента</span><span class="sxs-lookup"><span data-stu-id="f5f02-121">Required client settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/required-client-settings)
- [<span data-ttu-id="f5f02-122">Создание настраиваемого обработчика</span><span class="sxs-lookup"><span data-stu-id="f5f02-122">Writing your own customized handler</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/writing-your-own-customized-handler)
