---
title: Метод обновления (ADO)
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
# <a name="refresh-method-ado"></a><span data-ttu-id="e08d2-102">Метод обновления (ADO)</span><span class="sxs-lookup"><span data-stu-id="e08d2-102">Refresh method (ADO)</span></span>

<span data-ttu-id="e08d2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e08d2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e08d2-104">Обновляет объекты в коллекции, чтобы отражать объекты, доступные поставщику, и определенные для него.</span><span class="sxs-lookup"><span data-stu-id="e08d2-104">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="e08d2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e08d2-105">Syntax</span></span>

<span data-ttu-id="e08d2-106">*коллекция*. Обновление</span><span class="sxs-lookup"><span data-stu-id="e08d2-106">*collection*.Refresh</span></span>

## <a name="remarks"></a><span data-ttu-id="e08d2-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="e08d2-107">Remarks</span></span>

<span data-ttu-id="e08d2-108">Метод **Обновления** выполняет различные задачи в зависимости от коллекции, из которой он называется.</span><span class="sxs-lookup"><span data-stu-id="e08d2-108">The **Refresh** method accomplishes different tasks depending on the collection from which you call it.</span></span>

## <a name="parameters"></a><span data-ttu-id="e08d2-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="e08d2-109">Parameters</span></span>

<span data-ttu-id="e08d2-110">С помощью метода [](command-object-ado.md) **Обновления** в [](parameters-collection-ado.md) коллекции Параметры объекта Command извлекает сведения о параметрах поставщика для сохраненной процедуры или параметризованного запроса, указанного в **объекте Command.**</span><span class="sxs-lookup"><span data-stu-id="e08d2-110">Using the **Refresh** method on a [Command](command-object-ado.md) object's [Parameters](parameters-collection-ado.md) collection retrieves provider-side parameter information for the stored procedure or parameterized query specified in the **Command** object.</span></span> <span data-ttu-id="e08d2-111">Коллекция будет пустой для поставщиков, которые не поддерживают сохраненные вызовы процедур или параметризированные запросы.</span><span class="sxs-lookup"><span data-stu-id="e08d2-111">The collection will be empty for providers that do not support stored procedure calls or parameterized queries.</span></span>

<span data-ttu-id="e08d2-112">Перед вызовом метода Обновления необходимо  упредить [](connection-object-ado.md) свойство [ActiveConnection](activeconnection-property-ado.md) объекта Command допустимым объектом Подключения, свойство [CommandText](commandtext-property-ado.md) допустимой командой и свойство [CommandType](commandtype-property-ado.md) **adCmdStoredProc.** </span><span class="sxs-lookup"><span data-stu-id="e08d2-112">You should set the [ActiveConnection](activeconnection-property-ado.md) property of the **Command** object to a valid [Connection](connection-object-ado.md) object, the [CommandText](commandtext-property-ado.md) property to a valid command, and the [CommandType](commandtype-property-ado.md) property to **adCmdStoredProc** before calling the **Refresh** method.</span></span>

<span data-ttu-id="e08d2-113">Если вы имеете доступ к коллекции **Параметры** перед вызовом метода **Обновления,** ADO автоматически вызывает метод и заполняет коллекцию для вас.</span><span class="sxs-lookup"><span data-stu-id="e08d2-113">If you access the **Parameters** collection before calling the **Refresh** method, ADO will automatically call the method and populate the collection for you.</span></span>

> [!NOTE]
> <span data-ttu-id="e08d2-114">Если метод **Обновления** используется для получения сведений о параметрах от поставщика и [](parameter-object-ado.md) возвращает один или несколько объектов типа параметра переменной длины, ADO может выделять память для параметров в зависимости от их максимального потенциального размера, что приведет к ошибке во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="e08d2-114">If you use the **Refresh** method to obtain parameter information from the provider and it returns one or more variable-length data type [Parameter](parameter-object-ado.md) objects, ADO may allocate memory for the parameters based on their maximum potential size, which will cause an error during execution.</span></span> <span data-ttu-id="e08d2-115">Прежде чем вызывать метод [Execute,](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) чтобы предотвратить ошибки, необходимо явно задано свойство [Size](size-property-ado.md) для этих параметров.</span><span class="sxs-lookup"><span data-stu-id="e08d2-115">You should explicitly set the [Size](size-property-ado.md) property for these parameters before calling the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method to prevent errors.</span></span>

### <a name="fields"></a><span data-ttu-id="e08d2-116">Fields</span><span class="sxs-lookup"><span data-stu-id="e08d2-116">Fields</span></span>

<span data-ttu-id="e08d2-117">Использование метода **Обновления** в коллекции **Fields** не оказывает видимого эффекта.</span><span class="sxs-lookup"><span data-stu-id="e08d2-117">Using the **Refresh** method on the **Fields** collection has no visible effect.</span></span> <span data-ttu-id="e08d2-118">Чтобы получить изменения из структуры баз данных, необходимо использовать метод [Requery](requery-method-ado.md) или, если объект [Recordset](recordset-object-ado.md) не поддерживает закладки, метод [MoveFirst.](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)</span><span class="sxs-lookup"><span data-stu-id="e08d2-118">To retrieve changes from the underlying database structure, you must use either the [Requery](requery-method-ado.md) method or, if the [Recordset](recordset-object-ado.md) object does not support bookmarks, the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

### <a name="properties"></a><span data-ttu-id="e08d2-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="e08d2-119">Properties</span></span>

<span data-ttu-id="e08d2-120">Использование метода **Обновления** в коллекции **свойств** некоторых объектов заполняет коллекцию динамическими свойствами, которые предоставляет поставщик.</span><span class="sxs-lookup"><span data-stu-id="e08d2-120">Using the **Refresh** method on a **Properties** collection of some objects populates the collection with the dynamic properties that the provider exposes.</span></span> <span data-ttu-id="e08d2-121">Эти свойства предоставляют сведения о функциональных возможностях, определенных поставщику, за пределами встроенных свойств, поддерживаемых ADO.</span><span class="sxs-lookup"><span data-stu-id="e08d2-121">These properties provide information about functionality specific to the provider, beyond the built-in properties ADO supports.</span></span>

