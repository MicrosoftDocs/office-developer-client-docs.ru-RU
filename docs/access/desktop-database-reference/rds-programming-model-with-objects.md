---
title: RDS Programming Model with Objects
TOCTitle: RDS Programming Model with Objects
ms:assetid: 207150ec-8eb5-bec5-3059-db37a0e28c19
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248987(v=office.15)
ms:contentKeyID: 48543663
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 833d3676c8fa3fac1e5cb8e16477073cde611199
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480733"
---
# <a name="rds-programming-model-with-objects"></a><span data-ttu-id="c3d7a-102">RDS Programming Model with Objects</span><span class="sxs-lookup"><span data-stu-id="c3d7a-102">RDS Programming Model with Objects</span></span>


<span data-ttu-id="c3d7a-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c3d7a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c3d7a-104">Цель служб удаленных рабочих СТОЛОВ — получить доступ к и обновлять источники данных через промежуточное, таких как службы IIS.</span><span class="sxs-lookup"><span data-stu-id="c3d7a-104">The goal of RDS is to gain access to and update data sources through an intermediary such as IIS.</span></span> <span data-ttu-id="c3d7a-105">Модель программирования определяет последовательность действий, необходимых для этой цели.</span><span class="sxs-lookup"><span data-stu-id="c3d7a-105">The programming model specifies the sequence of activities necessary to accomplish this goal.</span></span> <span data-ttu-id="c3d7a-106">Объектная модель определяет объекты, методы и свойства влияют на модели программирования.</span><span class="sxs-lookup"><span data-stu-id="c3d7a-106">The object model specifies the objects whose methods and properties affect the programming model.</span></span>

<span data-ttu-id="c3d7a-107">Служб удаленных рабочих СТОЛОВ позволяет выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="c3d7a-107">RDS provides the means to perform the following sequence of actions:</span></span>

  - <span data-ttu-id="c3d7a-108">Укажите программу для вызова на сервере и получить способом (прокси-сервер), обратитесь к нему из клиента ([RDS. Пространства данных](dataspace-object-rds.md)).</span><span class="sxs-lookup"><span data-stu-id="c3d7a-108">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client ([RDS.DataSpace](dataspace-object-rds.md)).</span></span>

  - <span data-ttu-id="c3d7a-109">Вызов программы сервера.</span><span class="sxs-lookup"><span data-stu-id="c3d7a-109">Invoke the server program.</span></span> <span data-ttu-id="c3d7a-110">Передает параметры программе сервера, которое идентифицирует источник данных и команды для устранения проблемы (прокси-сервер или [RDS. DataControl](datacontrol-object-rds.md)).</span><span class="sxs-lookup"><span data-stu-id="c3d7a-110">Pass parameters to the server program that identifies the data source and the command to issue (proxy or [RDS.DataControl](datacontrol-object-rds.md)).</span></span>

  - <span data-ttu-id="c3d7a-111">Программы сервера получает объект [набора записей](recordset-object-ado.md) из источника данных, обычно с помощью ADO.</span><span class="sxs-lookup"><span data-stu-id="c3d7a-111">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO.</span></span> <span data-ttu-id="c3d7a-112">Кроме того в объект **набора записей** обрабатывается на сервере ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).</span><span class="sxs-lookup"><span data-stu-id="c3d7a-112">Optionally, the **Recordset** object is processed on the server ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).</span></span>

  - <span data-ttu-id="c3d7a-113">Программы сервера возвращает окончательный объекта **набора записей** в клиентском приложении (прокси-сервер).</span><span class="sxs-lookup"><span data-stu-id="c3d7a-113">The server program returns the final **Recordset** object to the client application (proxy).</span></span>

  - <span data-ttu-id="c3d7a-114">На стороне клиента, находится в состоянии объекта **набора записей** в форму, можно легко использовать visual элементы управления (элемент управления visual и **RDS. DataControl**).</span><span class="sxs-lookup"><span data-stu-id="c3d7a-114">On the client, the **Recordset** object is put into a form that can be easily used by visual controls (visual control and **RDS.DataControl**).</span></span>

  - <span data-ttu-id="c3d7a-115">Изменения в объект **набора записей** отправляются на сервер и используется для обновления источника данных (**RDS. DataControl** или **RDSServer.DataFactory**).</span><span class="sxs-lookup"><span data-stu-id="c3d7a-115">Changes to the **Recordset** object are sent back to the server and used to update the data source (**RDS.DataControl** or **RDSServer.DataFactory**).</span></span>

