---
title: Метод Refresh (ADO)
TOCTitle: Refresh method (ADO)
ms:assetid: f1c8829f-9c7d-12b6-7470-727ff38d663e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250227(v=office.15)
ms:contentKeyID: 48548631
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bd7c47e7c3e41a7b42571043cfafc9e4e909a9f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309259"
---
# <a name="refresh-method-ado"></a><span data-ttu-id="1f0dd-102">Метод Refresh (ADO)</span><span class="sxs-lookup"><span data-stu-id="1f0dd-102">Refresh method (ADO)</span></span>

<span data-ttu-id="1f0dd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f0dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f0dd-104">Обновляет объекты в коллекции, чтобы отразить объекты, доступные поставщику и соответствующие объекты.</span><span class="sxs-lookup"><span data-stu-id="1f0dd-104">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f0dd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f0dd-105">Syntax</span></span>

<span data-ttu-id="1f0dd-106">*коллекция*. Обновление</span><span class="sxs-lookup"><span data-stu-id="1f0dd-106">*collection*.Refresh</span></span>

## <a name="remarks"></a><span data-ttu-id="1f0dd-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="1f0dd-107">Remarks</span></span>

<span data-ttu-id="1f0dd-108">Метод **Refresh** выполняет различные задачи в зависимости от того, из какой коллекции он вызывается.</span><span class="sxs-lookup"><span data-stu-id="1f0dd-108">The **Refresh** method accomplishes different tasks depending on the collection from which you call it.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f0dd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f0dd-109">Parameters</span></span>

<span data-ttu-id="1f0dd-110">При использовании метода **Refresh** в коллекции [Parameters](parameters-collection-ado.md) объекта [Command](command-object-ado.md) извлекаются сведения о параметрах на стороне поставщика для хранимой процедуры или запроса с параметрами, указанными в объекте **Command** .</span><span class="sxs-lookup"><span data-stu-id="1f0dd-110">Using the **Refresh** method on a [Command](command-object-ado.md) object's [Parameters](parameters-collection-ado.md) collection retrieves provider-side parameter information for the stored procedure or parameterized query specified in the **Command** object.</span></span> <span data-ttu-id="1f0dd-111">Коллекция будет пустой для поставщиков, которые не поддерживают вызовы хранимых процедур или параметризованные запросы.</span><span class="sxs-lookup"><span data-stu-id="1f0dd-111">The collection will be empty for providers that do not support stored procedure calls or parameterized queries.</span></span>

<span data-ttu-id="1f0dd-112">Необходимо задать для свойства [ActiveConnection](activeconnection-property-ado.md) объекта **Command** допустимый объект [Connection](connection-object-ado.md) , свойство [CommandText](commandtext-property-ado.md) для допустимой команды, а свойство [CommandType](commandtype-property-ado.md) — **адкмдсторедпрок** перед вызовом метода **Refresh** .</span><span class="sxs-lookup"><span data-stu-id="1f0dd-112">You should set the [ActiveConnection](activeconnection-property-ado.md) property of the **Command** object to a valid [Connection](connection-object-ado.md) object, the [CommandText](commandtext-property-ado.md) property to a valid command, and the [CommandType](commandtype-property-ado.md) property to **adCmdStoredProc** before calling the **Refresh** method.</span></span>

<span data-ttu-id="1f0dd-113">Если вы обращаетесь к коллекции **Parameters** перед вызовом метода **Refresh** , ADO автоматически вызывает метод и заполняет коллекцию.</span><span class="sxs-lookup"><span data-stu-id="1f0dd-113">If you access the **Parameters** collection before calling the **Refresh** method, ADO will automatically call the method and populate the collection for you.</span></span>

> [!NOTE]
> <span data-ttu-id="1f0dd-114">Если вы используете метод **Refresh** для получения сведений о параметрах от поставщика и возвращает один или несколько объектов [параметров](parameter-object-ado.md) типа данных переменной длины, ADO может выделить память для параметров на основе максимально возможного размера, что приведет к ошибке во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="1f0dd-114">If you use the **Refresh** method to obtain parameter information from the provider and it returns one or more variable-length data type [Parameter](parameter-object-ado.md) objects, ADO may allocate memory for the parameters based on their maximum potential size, which will cause an error during execution.</span></span> <span data-ttu-id="1f0dd-115">Необходимо явно задать свойство [size](size-property-ado.md) для этих параметров перед вызовом метода [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) для предотвращения ошибок.</span><span class="sxs-lookup"><span data-stu-id="1f0dd-115">You should explicitly set the [Size](size-property-ado.md) property for these parameters before calling the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method to prevent errors.</span></span>

### <a name="fields"></a><span data-ttu-id="1f0dd-116">Fields</span><span class="sxs-lookup"><span data-stu-id="1f0dd-116">Fields</span></span>

<span data-ttu-id="1f0dd-117">Использование метода **Refresh** в коллекции **Fields** не имеет видимого результата.</span><span class="sxs-lookup"><span data-stu-id="1f0dd-117">Using the **Refresh** method on the **Fields** collection has no visible effect.</span></span> <span data-ttu-id="1f0dd-118">Чтобы получить изменения из базовой структуры базы данных, необходимо использовать метод [Requery](requery-method-ado.md) либо, если объект [Recordset](recordset-object-ado.md) не поддерживает закладки, метод [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1f0dd-118">To retrieve changes from the underlying database structure, you must use either the [Requery](requery-method-ado.md) method or, if the [Recordset](recordset-object-ado.md) object does not support bookmarks, the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

### <a name="properties"></a><span data-ttu-id="1f0dd-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="1f0dd-119">Properties</span></span>

<span data-ttu-id="1f0dd-120">Использование метода **Refresh** для коллекции **свойств** некоторых объектов заполняет коллекцию динамическими свойствами, предоставляемыми поставщиком.</span><span class="sxs-lookup"><span data-stu-id="1f0dd-120">Using the **Refresh** method on a **Properties** collection of some objects populates the collection with the dynamic properties that the provider exposes.</span></span> <span data-ttu-id="1f0dd-121">Эти свойства предоставляют сведения о функциональных возможностях, характерных для поставщика, Кроме встроенных свойств ADO.</span><span class="sxs-lookup"><span data-stu-id="1f0dd-121">These properties provide information about functionality specific to the provider, beyond the built-in properties ADO supports.</span></span>

