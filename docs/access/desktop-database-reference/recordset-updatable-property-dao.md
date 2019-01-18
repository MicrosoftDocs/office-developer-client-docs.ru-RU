---
title: Свойство Recordset.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 2d4bdcef-1b10-b542-ce0f-6172c271131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192110(v=office.15)
ms:contentKeyID: 48543968
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 722ccc2334cd00ed89a1193709023db039ba9fd3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712920"
---
# <a name="recordsetupdatable-property-dao"></a><span data-ttu-id="eb2aa-102">Свойство Recordset.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="eb2aa-102">Recordset.Updatable property (DAO)</span></span>


<span data-ttu-id="eb2aa-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb2aa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eb2aa-104">Возвращает значение, указывающее, является ли объект DAO можно изменить.</span><span class="sxs-lookup"><span data-stu-id="eb2aa-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="eb2aa-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="eb2aa-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb2aa-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb2aa-106">Syntax</span></span>

<span data-ttu-id="eb2aa-107">*выражение* . Обновляемые</span><span class="sxs-lookup"><span data-stu-id="eb2aa-107">*expression* .Updatable</span></span>

<span data-ttu-id="eb2aa-108">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="eb2aa-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb2aa-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="eb2aa-109">Remarks</span></span>

<span data-ttu-id="eb2aa-110">Моментальный снимок и прямого только – набора записей объекты типа всегда возвращает **значение False**.</span><span class="sxs-lookup"><span data-stu-id="eb2aa-110">Snapshot- and forward-only–type Recordset objects always return **False**.</span></span>

<span data-ttu-id="eb2aa-111">Несколько типов объектов может содержать поля, которые не могут быть обновлены.</span><span class="sxs-lookup"><span data-stu-id="eb2aa-111">Many types of objects can contain fields that can't be updated.</span></span> <span data-ttu-id="eb2aa-112">Например можно создать объект типа динамического **набора записей** , в котором можно изменить только некоторые поля.</span><span class="sxs-lookup"><span data-stu-id="eb2aa-112">For example, you can create a dynaset-type **Recordset** object in which only some fields can be changed.</span></span> <span data-ttu-id="eb2aa-113">Эти поля устранения или содержат данные, автоматически увеличивает или динамический набор может привести к из запроса, который объединяет обновляемых и nonupdatable таблицы.</span><span class="sxs-lookup"><span data-stu-id="eb2aa-113">These fields can be fixed or contain data that increments automatically, or the dynaset can result from a query that combines updatable and nonupdatable tables.</span></span>

<span data-ttu-id="eb2aa-114">Если объект содержит поля только для чтения, значение свойства **с возможностью записи** имеет **значение False**.</span><span class="sxs-lookup"><span data-stu-id="eb2aa-114">If the object contains only read-only fields, the value of the **Updatable** property is **False**.</span></span> <span data-ttu-id="eb2aa-115">Когда обновляемых одно или несколько полей, значение свойства — **True**.</span><span class="sxs-lookup"><span data-stu-id="eb2aa-115">When one or more fields are updatable, the property's value is **True**.</span></span> <span data-ttu-id="eb2aa-116">Можно изменить только обновляемых полей.</span><span class="sxs-lookup"><span data-stu-id="eb2aa-116">You can edit only the updatable fields.</span></span> <span data-ttu-id="eb2aa-117">Перехватываемые ошибка возникает при попытке присвоить новое значение в поле только для чтения.</span><span class="sxs-lookup"><span data-stu-id="eb2aa-117">A trappable error occurs if you try to assign a new value to a read-only field.</span></span>

<span data-ttu-id="eb2aa-118">Обновляемый объект может содержать поля только для чтения, перед изменить запись проверьте свойство **DataUpdatable** каждое поле в коллекции **полей** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="eb2aa-118">Because an updatable object can contain read-only fields, check the **DataUpdatable** property of each field in the **Fields** collection of a **Recordset** object before you edit a record.</span></span>

