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
# <a name="rds-programming-model-with-objects"></a><span data-ttu-id="89d2c-102">Модель программирования RDS с объектами</span><span class="sxs-lookup"><span data-stu-id="89d2c-102">RDS programming model with objects</span></span>

<span data-ttu-id="89d2c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89d2c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="89d2c-104">Цель RDS — получить доступ к источникам данных и обновить их через посредника, например IIS.</span><span class="sxs-lookup"><span data-stu-id="89d2c-104">The goal of RDS is to gain access to and update data sources through an intermediary such as IIS.</span></span> <span data-ttu-id="89d2c-105">Модель программирования указывает последовательность действий, необходимых для достижения этой цели.</span><span class="sxs-lookup"><span data-stu-id="89d2c-105">The programming model specifies the sequence of activities necessary to accomplish this goal.</span></span> <span data-ttu-id="89d2c-106">Объектная модель указывает объекты, методы и свойства которых влияют на модель программирования.</span><span class="sxs-lookup"><span data-stu-id="89d2c-106">The object model specifies the objects whose methods and properties affect the programming model.</span></span>

<span data-ttu-id="89d2c-107">RDS предоставляет средства для выполнения следующей последовательности действий:</span><span class="sxs-lookup"><span data-stu-id="89d2c-107">RDS provides the means to perform the following sequence of actions:</span></span>

- <span data-ttu-id="89d2c-108">Укажите программу, вызываемую на сервере, и получите способ (прокси) ссылаться на нее от клиента[(RDS). DataSpace](dataspace-object-rds.md)).</span><span class="sxs-lookup"><span data-stu-id="89d2c-108">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client ([RDS.DataSpace](dataspace-object-rds.md)).</span></span>

- <span data-ttu-id="89d2c-109">Вызов серверной программы.</span><span class="sxs-lookup"><span data-stu-id="89d2c-109">Invoke the server program.</span></span> <span data-ttu-id="89d2c-110">Передай параметры серверной программе, которая идентифицирует источник данных и команду для выпуска (прокси или [RDS. DataControl](datacontrol-object-rds.md)).</span><span class="sxs-lookup"><span data-stu-id="89d2c-110">Pass parameters to the server program that identifies the data source and the command to issue (proxy or [RDS.DataControl](datacontrol-object-rds.md)).</span></span>

- <span data-ttu-id="89d2c-111">Серверная программа получает объект [Recordset](recordset-object-ado.md) из источника данных, как правило, с помощью ADO.</span><span class="sxs-lookup"><span data-stu-id="89d2c-111">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO.</span></span> <span data-ttu-id="89d2c-112">Необязательный объект **Recordset** обрабатывается на сервере [(RDSServer.DataFactory).](datafactory-object-rdsserver.md)</span><span class="sxs-lookup"><span data-stu-id="89d2c-112">Optionally, the **Recordset** object is processed on the server ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).</span></span>

- <span data-ttu-id="89d2c-113">Программа сервера возвращает конечный объект **Recordset** в клиентском приложении (прокси).</span><span class="sxs-lookup"><span data-stu-id="89d2c-113">The server program returns the final **Recordset** object to the client application (proxy).</span></span>

- <span data-ttu-id="89d2c-114">На клиенте объект **Recordset** вложен в форму, которую можно легко использовать с помощью визуальных элементов управления (визуального управления и **RDS). DataControl**).</span><span class="sxs-lookup"><span data-stu-id="89d2c-114">On the client, the **Recordset** object is put into a form that can be easily used by visual controls (visual control and **RDS.DataControl**).</span></span>

- <span data-ttu-id="89d2c-115">Изменения объекта **Recordset** отправляются обратно на сервер и используются для обновления источника данных **(RDS). DataControl** или **RDSServer.DataFactory**).</span><span class="sxs-lookup"><span data-stu-id="89d2c-115">Changes to the **Recordset** object are sent back to the server and used to update the data source (**RDS.DataControl** or **RDSServer.DataFactory**).</span></span>

