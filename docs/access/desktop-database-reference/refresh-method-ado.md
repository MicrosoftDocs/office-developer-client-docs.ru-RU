---
title: Обновления метода (ADO)
TOCTitle: Refresh Method (ADO)
ms:assetid: f1c8829f-9c7d-12b6-7470-727ff38d663e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250227(v=office.15)
ms:contentKeyID: 48548631
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 710329fb00615b127ee5bc79cb10a6b5fc71b5e0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875674"
---
# <a name="refresh-method-ado"></a><span data-ttu-id="acbd8-102">Обновления метода (ADO)</span><span class="sxs-lookup"><span data-stu-id="acbd8-102">Refresh Method (ADO)</span></span>


<span data-ttu-id="acbd8-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="acbd8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="acbd8-104">Обновление объектов в коллекции объектов, доступных из и относящиеся к поставщику.</span><span class="sxs-lookup"><span data-stu-id="acbd8-104">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="acbd8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="acbd8-105">Syntax</span></span>

<span data-ttu-id="acbd8-106">*семейства сайтов*. Обновление</span><span class="sxs-lookup"><span data-stu-id="acbd8-106">*collection*.Refresh</span></span>

## <a name="remarks"></a><span data-ttu-id="acbd8-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="acbd8-107">Remarks</span></span>

<span data-ttu-id="acbd8-108">Метод **Refresh** выполняет различные задачи в зависимости от семейства сайтов, из которого вызывается его.</span><span class="sxs-lookup"><span data-stu-id="acbd8-108">The **Refresh** method accomplishes different tasks depending on the collection from which you call it.</span></span>

## <a name="parameters"></a><span data-ttu-id="acbd8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="acbd8-109">Parameters</span></span>

<span data-ttu-id="acbd8-110">С помощью метода **обновления** на коллекцию [параметров](parameters-collection-ado.md) объекта [команда](command-object-ado.md) получает сведения о параметрах стороне поставщика для хранимой процедуры или параметризованный запрос, указанный в объекте **команды** .</span><span class="sxs-lookup"><span data-stu-id="acbd8-110">Using the **Refresh** method on a [Command](command-object-ado.md) object's [Parameters](parameters-collection-ado.md) collection retrieves provider-side parameter information for the stored procedure or parameterized query specified in the **Command** object.</span></span> <span data-ttu-id="acbd8-111">Коллекция будет пустым для поставщиков, которые не поддерживают вызовы хранимых процедур и запросов с заданными параметрами.</span><span class="sxs-lookup"><span data-stu-id="acbd8-111">The collection will be empty for providers that do not support stored procedure calls or parameterized queries.</span></span>

<span data-ttu-id="acbd8-112">Должно значение свойства [ActiveConnection](activeconnection-property-ado.md) объекта **команды** на допустимый объект [подключения](connection-object-ado.md) , свойства [CommandText](commandtext-property-ado.md) допустимой команды и свойства [CommandType](commandtype-property-ado.md) **adCmdStoredProc** перед вызов метода **обновления** .</span><span class="sxs-lookup"><span data-stu-id="acbd8-112">You should set the [ActiveConnection](activeconnection-property-ado.md) property of the **Command** object to a valid [Connection](connection-object-ado.md) object, the [CommandText](commandtext-property-ado.md) property to a valid command, and the [CommandType](commandtype-property-ado.md) property to **adCmdStoredProc** before calling the **Refresh** method.</span></span>

<span data-ttu-id="acbd8-113">Если доступ к коллекции **параметров** до вызова метода **обновления на** ADO автоматически вызовите метод и заполнения в коллекции.</span><span class="sxs-lookup"><span data-stu-id="acbd8-113">If you access the **Parameters** collection before calling the **Refresh** method, ADO will automatically call the method and populate the collection for you.</span></span>


> [!NOTE]
> <P><span data-ttu-id="acbd8-114">Если использовать метод <STRONG>Refresh</STRONG> для получения сведений о параметрах от поставщика, и он возвращает тип данных переменной длины один или несколько объектов <A href="parameter-object-ado.md">параметров</A> , ADO может выделить память для параметров, основанных на их максимальный размер потенциальных, который будет возникает ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="acbd8-114">If you use the <STRONG>Refresh</STRONG> method to obtain parameter information from the provider and it returns one or more variable-length data type <A href="parameter-object-ado.md">Parameter</A> objects, ADO may allocate memory for the parameters based on their maximum potential size, which will cause an error during execution.</span></span> <span data-ttu-id="acbd8-115">Необходимо явно задать свойство <A href="size-property-ado.md">размер</A> для этих параметров до вызова метода <A href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute</A> для предотвращения ошибок.</span><span class="sxs-lookup"><span data-stu-id="acbd8-115">You should explicitly set the <A href="size-property-ado.md">Size</A> property for these parameters before calling the <A href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute</A> method to prevent errors.</span></span></P>



<span data-ttu-id="acbd8-116">**Поля**</span><span class="sxs-lookup"><span data-stu-id="acbd8-116">**Fields**</span></span>

<span data-ttu-id="acbd8-117">С помощью метода **обновления** на коллекции **полей** не действует видимым.</span><span class="sxs-lookup"><span data-stu-id="acbd8-117">Using the **Refresh** method on the **Fields** collection has no visible effect.</span></span> <span data-ttu-id="acbd8-118">Чтобы извлечь изменения из базовой структуры базы данных, необходимо использовать либо метод [повторный запрос](requery-method-ado.md) или, если объекта [набора записей](recordset-object-ado.md) не поддерживает закладки, метод [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="acbd8-118">To retrieve changes from the underlying database structure, you must use either the [Requery](requery-method-ado.md) method or, if the [Recordset](recordset-object-ado.md) object does not support bookmarks, the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

<span data-ttu-id="acbd8-119">**Свойства**</span><span class="sxs-lookup"><span data-stu-id="acbd8-119">**Properties**</span></span>

<span data-ttu-id="acbd8-120">С помощью метода **обновления** на коллекцию **свойств** некоторые объекты заполняет коллекцию динамические свойства, предоставляемые поставщиком.</span><span class="sxs-lookup"><span data-stu-id="acbd8-120">Using the **Refresh** method on a **Properties** collection of some objects populates the collection with the dynamic properties that the provider exposes.</span></span> <span data-ttu-id="acbd8-121">Эти свойства предоставляют сведения о конкретных функциях к поставщику за пределы для поддержки ADO встроенных свойств.</span><span class="sxs-lookup"><span data-stu-id="acbd8-121">These properties provide information about functionality specific to the provider, beyond the built-in properties ADO supports.</span></span>

