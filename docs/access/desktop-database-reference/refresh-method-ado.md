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
# <a name="refresh-method-ado"></a><span data-ttu-id="04961-102">Метод Refresh (ADO)</span><span class="sxs-lookup"><span data-stu-id="04961-102">Refresh method (ADO)</span></span>

<span data-ttu-id="04961-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="04961-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04961-104">Обновляет объекты в коллекции, чтобы отразить объекты, доступные поставщику и относяющиеся к конкретному поставщику.</span><span class="sxs-lookup"><span data-stu-id="04961-104">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="04961-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04961-105">Syntax</span></span>

<span data-ttu-id="04961-106">*collection*. Обновление</span><span class="sxs-lookup"><span data-stu-id="04961-106">*collection*.Refresh</span></span>

## <a name="remarks"></a><span data-ttu-id="04961-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="04961-107">Remarks</span></span>

<span data-ttu-id="04961-108">Метод **Refresh** выполняет различные задачи в зависимости от коллекции, из которой он вызываем.</span><span class="sxs-lookup"><span data-stu-id="04961-108">The **Refresh** method accomplishes different tasks depending on the collection from which you call it.</span></span>

## <a name="parameters"></a><span data-ttu-id="04961-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="04961-109">Parameters</span></span>

<span data-ttu-id="04961-110">Использование метода **Refresh** в коллекции [параметров](parameters-collection-ado.md) объекта [Command](command-object-ado.md) извлекает сведения о параметрах на стороне поставщика для хранимой процедуры или параметризованного запроса, указанного в **объекте Command.**</span><span class="sxs-lookup"><span data-stu-id="04961-110">Using the **Refresh** method on a [Command](command-object-ado.md) object's [Parameters](parameters-collection-ado.md) collection retrieves provider-side parameter information for the stored procedure or parameterized query specified in the **Command** object.</span></span> <span data-ttu-id="04961-111">Коллекция будет пустой для поставщиков, которые не поддерживают хранимые вызовы процедур или параметризованные запросы.</span><span class="sxs-lookup"><span data-stu-id="04961-111">The collection will be empty for providers that do not support stored procedure calls or parameterized queries.</span></span>

<span data-ttu-id="04961-112">Перед вызовом метода **Refresh** необходимо установить для свойства [ActiveConnection](activeconnection-property-ado.md) объекта **Command** допустимый объект [Connection,](connection-object-ado.md) для свойства [CommandText](commandtext-property-ado.md) допустимую команду и свойство [CommandType](commandtype-property-ado.md) для **adCmdStoredProc.**</span><span class="sxs-lookup"><span data-stu-id="04961-112">You should set the [ActiveConnection](activeconnection-property-ado.md) property of the **Command** object to a valid [Connection](connection-object-ado.md) object, the [CommandText](commandtext-property-ado.md) property to a valid command, and the [CommandType](commandtype-property-ado.md) property to **adCmdStoredProc** before calling the **Refresh** method.</span></span>

<span data-ttu-id="04961-113">При доступе к коллекции **Parameters** перед вызовом метода **Refresh** ADO автоматически вызывает метод и заполняет коллекцию автоматически.</span><span class="sxs-lookup"><span data-stu-id="04961-113">If you access the **Parameters** collection before calling the **Refresh** method, ADO will automatically call the method and populate the collection for you.</span></span>

> [!NOTE]
> <span data-ttu-id="04961-114">Если метод **Refresh** используется для получения сведений о параметрах от поставщика и [](parameter-object-ado.md) возвращает один или несколько объектов parameter типа данных переменной длины, ADO может выделить память для параметров в зависимости от их максимального потенциального размера, что приведет к ошибке во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="04961-114">If you use the **Refresh** method to obtain parameter information from the provider and it returns one or more variable-length data type [Parameter](parameter-object-ado.md) objects, ADO may allocate memory for the parameters based on their maximum potential size, which will cause an error during execution.</span></span> <span data-ttu-id="04961-115">Перед вызовом метода [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) необходимо явно установить свойство [Size](size-property-ado.md) для этих параметров, чтобы предотвратить ошибки.</span><span class="sxs-lookup"><span data-stu-id="04961-115">You should explicitly set the [Size](size-property-ado.md) property for these parameters before calling the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method to prevent errors.</span></span>

### <a name="fields"></a><span data-ttu-id="04961-116">Поля</span><span class="sxs-lookup"><span data-stu-id="04961-116">Fields</span></span>

<span data-ttu-id="04961-117">Использование метода **Refresh** для коллекции **Fields** не оказывает видимого эффекта.</span><span class="sxs-lookup"><span data-stu-id="04961-117">Using the **Refresh** method on the **Fields** collection has no visible effect.</span></span> <span data-ttu-id="04961-118">Чтобы получить изменения из структуры баз данных, необходимо использовать либо метод [Requery,](requery-method-ado.md) либо, если объект [Recordset](recordset-object-ado.md) не поддерживает закладки, [метод MoveFirst.](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)</span><span class="sxs-lookup"><span data-stu-id="04961-118">To retrieve changes from the underlying database structure, you must use either the [Requery](requery-method-ado.md) method or, if the [Recordset](recordset-object-ado.md) object does not support bookmarks, the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

### <a name="properties"></a><span data-ttu-id="04961-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="04961-119">Properties</span></span>

<span data-ttu-id="04961-120">Использование метода **Refresh** для коллекции **свойств** некоторых объектов заполняет коллекцию динамическими свойствами, которые предоставляет поставщик.</span><span class="sxs-lookup"><span data-stu-id="04961-120">Using the **Refresh** method on a **Properties** collection of some objects populates the collection with the dynamic properties that the provider exposes.</span></span> <span data-ttu-id="04961-121">Эти свойства предоставляют сведения о функциях, характерных для поставщика, помимо встроенных свойств, поддерживаемых ADO.</span><span class="sxs-lookup"><span data-stu-id="04961-121">These properties provide information about functionality specific to the provider, beyond the built-in properties ADO supports.</span></span>

