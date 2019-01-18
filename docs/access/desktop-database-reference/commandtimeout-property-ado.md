---
title: Свойство CommandTimeout (ADO)
TOCTitle: CommandTimeout property (ADO)
ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15)
ms:contentKeyID: 48546714
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9d44bc8fae0143b183ef54120cdaaf91337f36f8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700117"
---
# <a name="commandtimeout-property-ado"></a><span data-ttu-id="86e20-102">Свойство CommandTimeout (ADO)</span><span class="sxs-lookup"><span data-stu-id="86e20-102">CommandTimeout property (ADO)</span></span>


<span data-ttu-id="86e20-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="86e20-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86e20-104">Указывает время ожидания при выполнении команды перед завершается и генерируется ошибка.</span><span class="sxs-lookup"><span data-stu-id="86e20-104">Indicates how long to wait while executing a command before terminating the attempt and generating an error.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="86e20-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="86e20-105">Settings and return values</span></span>

<span data-ttu-id="86e20-106">Задает или возвращает значение типа **Long** , указывающее, в секундах, как долго следует ожидать выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="86e20-106">Sets or returns a **Long** value that indicates, in seconds, how long to wait for a command to execute.</span></span> <span data-ttu-id="86e20-107">Значение по умолчанию — 30.</span><span class="sxs-lookup"><span data-stu-id="86e20-107">Default is 30.</span></span>

## <a name="remarks"></a><span data-ttu-id="86e20-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="86e20-108">Remarks</span></span>

<span data-ttu-id="86e20-109">Используйте свойство **CommandTimeout** объекта [подключения](connection-object-ado.md) или [команду](command-object-ado.md) чтобы разрешить отмены для вызова метода [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) , из-за задержки от. Используйте сетевой трафик или высокая интенсивность операций сервера.</span><span class="sxs-lookup"><span data-stu-id="86e20-109">Use the **CommandTimeout** property on a [Connection](connection-object-ado.md) object or [Command](command-object-ado.md) object to allow the cancellation of an [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method call, due to delays from network traffic or heavy server use.</span></span> <span data-ttu-id="86e20-110">Если в свойстве **CommandTimeout** этого времени до завершения выполнения команды, возникает ошибка, и ADO отменяет команду.</span><span class="sxs-lookup"><span data-stu-id="86e20-110">If the interval set in the **CommandTimeout** property elapses before the command completes execution, an error occurs and ADO cancels the command.</span></span> <span data-ttu-id="86e20-111">Если задать свойству присваивается значение 0, ADO ожидает неопределенное время до завершения выполнения.</span><span class="sxs-lookup"><span data-stu-id="86e20-111">If you set the property to zero, ADO will wait indefinitely until the execution is complete.</span></span> <span data-ttu-id="86e20-112">Убедитесь, что источник поставщика и данных, к которому написании кода поддержки **CommandTimeout** функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="86e20-112">Make sure the provider and data source to which you are writing code support the **CommandTimeout** functionality.</span></span>

<span data-ttu-id="86e20-113">Параметр **CommandTimeout** на объект **подключения** не оказывает влияния на параметр **CommandTimeout** объекта **команды** на том же **подключения**; то есть свойство **CommandTimeout** объект **команды** не наследует значение **CommandTimeout** объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="86e20-113">The **CommandTimeout** setting on a **Connection** object has no effect on the **CommandTimeout** setting on a **Command** object on the same **Connection**; that is, the **Command** object's **CommandTimeout** property does not inherit the value of the **Connection** object's **CommandTimeout** value.</span></span>

<span data-ttu-id="86e20-114">На объект **подключения** свойство **CommandTimeout** остается чтения/записи после открытия **подключения** .</span><span class="sxs-lookup"><span data-stu-id="86e20-114">On a **Connection** object, the **CommandTimeout** property remains read/write after the **Connection** is opened.</span></span>

