---
title: Модель программирования RDS с объектами
TOCTitle: RDS programming model with objects
ms:assetid: 207150ec-8eb5-bec5-3059-db37a0e28c19
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248987(v=office.15)
ms:contentKeyID: 48543663
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9743fb1e7329457abb60ed8ed41bc39067f3551d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301052"
---
# <a name="rds-programming-model-with-objects"></a><span data-ttu-id="87e4e-102">Модель программирования RDS с объектами</span><span class="sxs-lookup"><span data-stu-id="87e4e-102">RDS programming model with objects</span></span>

<span data-ttu-id="87e4e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="87e4e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="87e4e-104">Задача RDS заключается в том, чтобы получать доступ к источникам данных и обновлять их с помощью промежуточных посредников, таких как IIS.</span><span class="sxs-lookup"><span data-stu-id="87e4e-104">The goal of RDS is to gain access to and update data sources through an intermediary such as IIS.</span></span> <span data-ttu-id="87e4e-105">Модель программирования указывает последовательность действий, необходимых для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="87e4e-105">The programming model specifies the sequence of activities necessary to accomplish this goal.</span></span> <span data-ttu-id="87e4e-106">Объектная модель указывает объекты, методы и свойства которых влияют на модель программирования.</span><span class="sxs-lookup"><span data-stu-id="87e4e-106">The object model specifies the objects whose methods and properties affect the programming model.</span></span>

<span data-ttu-id="87e4e-107">RDS предоставляет средства для выполнения следующей последовательности действий:</span><span class="sxs-lookup"><span data-stu-id="87e4e-107">RDS provides the means to perform the following sequence of actions:</span></span>

- <span data-ttu-id="87e4e-108">Укажите программу, которая будет вызываться на сервере, и получите способ (прокси) для ссылки на него из клиента ([RDS. Пространство для ввода](dataspace-object-rds.md)).</span><span class="sxs-lookup"><span data-stu-id="87e4e-108">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client ([RDS.DataSpace](dataspace-object-rds.md)).</span></span>

- <span data-ttu-id="87e4e-109">Вызов серверной программы.</span><span class="sxs-lookup"><span data-stu-id="87e4e-109">Invoke the server program.</span></span> <span data-ttu-id="87e4e-110">Передача параметров в серверную программу, определяющую источник данных, и выполняемая команда (прокси или [RDS. Элемент управления](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="87e4e-110">Pass parameters to the server program that identifies the data source and the command to issue (proxy or [RDS.DataControl](datacontrol-object-rds.md)).</span></span>

- <span data-ttu-id="87e4e-111">Серверная программа получает объект [Recordset](recordset-object-ado.md) из источника данных, как правило, с помощью ADO.</span><span class="sxs-lookup"><span data-stu-id="87e4e-111">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO.</span></span> <span data-ttu-id="87e4e-112">При необходимости объект **Recordset** обрабатывается на сервере ([рдссервер.](datafactory-object-rdsserver.md)DataObject).</span><span class="sxs-lookup"><span data-stu-id="87e4e-112">Optionally, the **Recordset** object is processed on the server ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).</span></span>

- <span data-ttu-id="87e4e-113">Серверная программа возвращает конечный объект **Recordset** клиентскому приложению (прокси).</span><span class="sxs-lookup"><span data-stu-id="87e4e-113">The server program returns the final **Recordset** object to the client application (proxy).</span></span>

- <span data-ttu-id="87e4e-114">В клиенте объект **Recordset** помещается в форму, которая может быть легко использоваться визуальными элементами управления (визуальным элементом управления и **RDS. Элемент управления**.</span><span class="sxs-lookup"><span data-stu-id="87e4e-114">On the client, the **Recordset** object is put into a form that can be easily used by visual controls (visual control and **RDS.DataControl**).</span></span>

- <span data-ttu-id="87e4e-115">Изменения объекта **Recordset** отправляются обратно на сервер и используются для обновления источника данных (**RDS. Элемент управления** **Рдссервер или. факты**).</span><span class="sxs-lookup"><span data-stu-id="87e4e-115">Changes to the **Recordset** object are sent back to the server and used to update the data source (**RDS.DataControl** or **RDSServer.DataFactory**).</span></span>

