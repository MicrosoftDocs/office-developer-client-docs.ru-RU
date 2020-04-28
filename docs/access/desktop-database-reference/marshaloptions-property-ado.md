---
title: Свойство MarshalOptions (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 22a3662d3d14dd639069fa7aa48eda6f032fd2d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289772"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="a5364-102">Свойство MarshalOptions (ADO)</span><span class="sxs-lookup"><span data-stu-id="a5364-102">MarshalOptions property (ADO)</span></span>


<span data-ttu-id="a5364-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5364-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a5364-104">Указывает, какие записи необходимо упаковать обратно на сервер.</span><span class="sxs-lookup"><span data-stu-id="a5364-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a5364-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a5364-105">Settings And Return Values</span></span>

<span data-ttu-id="a5364-106">Задает или возвращает значение [маршалоптионсенум](marshaloptionsenum.md) .</span><span class="sxs-lookup"><span data-stu-id="a5364-106">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value.</span></span> <span data-ttu-id="a5364-107">Значение по умолчанию — **адмаршалалл**.</span><span class="sxs-lookup"><span data-stu-id="a5364-107">The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5364-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="a5364-108">Remarks</span></span>

<span data-ttu-id="a5364-109">При использовании [набора записей](recordset-object-ado.md)на стороне клиента записи, которые были изменены в клиенте, записываются обратно на средний уровень или на веб-сервер с помощью технологии, которая называется маршалингом, процесс упаковки и отправки параметров метода интерфейса для границ потоков или процессов.</span><span class="sxs-lookup"><span data-stu-id="a5364-109">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</span></span> <span data-ttu-id="a5364-110">Установка свойства **MarshalOptions** может поспособствовать повышению производительности при маршалинге измененных удаленных данных для обратного обновления на среднем уровне или на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="a5364-110">Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or web server.</span></span>

<span data-ttu-id="a5364-111">**Использование удаленной службы данных** Это свойство используется только в **наборе записей**на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="a5364-111">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>

