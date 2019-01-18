---
title: Свойство Recordset2.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: ad8184b6-ffe3-dde6-ddee-4b23cdaa9c59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821726(v=office.15)
ms:contentKeyID: 48547041
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b6e6f2a20b4779259b80eff1fc152abe3698217
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722069"
---
# <a name="recordset2updatable-property-dao"></a><span data-ttu-id="1fc61-102">Свойство Recordset2.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="1fc61-102">Recordset2.Updatable property (DAO)</span></span>


<span data-ttu-id="1fc61-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1fc61-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1fc61-104">Возвращает значение, указывающее, является ли объект DAO можно изменить.</span><span class="sxs-lookup"><span data-stu-id="1fc61-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="1fc61-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="1fc61-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc61-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fc61-106">Syntax</span></span>

<span data-ttu-id="1fc61-107">*выражение* . Обновляемые</span><span class="sxs-lookup"><span data-stu-id="1fc61-107">*expression* .Updatable</span></span>

<span data-ttu-id="1fc61-108">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="1fc61-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fc61-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="1fc61-109">Remarks</span></span>

<span data-ttu-id="1fc61-110">Моментальный снимок и прямого только – набора записей объекты типа всегда возвращает **значение False**.</span><span class="sxs-lookup"><span data-stu-id="1fc61-110">Snapshot- and forward-only–type Recordset objects always return **False**.</span></span>

<span data-ttu-id="1fc61-111">Несколько типов объектов может содержать поля, которые не могут быть обновлены.</span><span class="sxs-lookup"><span data-stu-id="1fc61-111">Many types of objects can contain fields that can't be updated.</span></span> <span data-ttu-id="1fc61-112">Например можно создать объект типа динамического **набора записей** , в котором можно изменить только некоторые поля.</span><span class="sxs-lookup"><span data-stu-id="1fc61-112">For example, you can create a dynaset-type **Recordset** object in which only some fields can be changed.</span></span> <span data-ttu-id="1fc61-113">Эти поля устранения или содержат данные, автоматически увеличивает или динамический набор может привести к из запроса, который объединяет обновляемых и nonupdatable таблицы.</span><span class="sxs-lookup"><span data-stu-id="1fc61-113">These fields can be fixed or contain data that increments automatically, or the dynaset can result from a query that combines updatable and nonupdatable tables.</span></span>

<span data-ttu-id="1fc61-114">Если объект содержит поля только для чтения, значение свойства **с возможностью записи** имеет **значение False**.</span><span class="sxs-lookup"><span data-stu-id="1fc61-114">If the object contains only read-only fields, the value of the **Updatable** property is **False**.</span></span> <span data-ttu-id="1fc61-115">Когда обновляемых одно или несколько полей, значение свойства — **True**.</span><span class="sxs-lookup"><span data-stu-id="1fc61-115">When one or more fields are updatable, the property's value is **True**.</span></span> <span data-ttu-id="1fc61-116">Можно изменить только обновляемых полей.</span><span class="sxs-lookup"><span data-stu-id="1fc61-116">You can edit only the updatable fields.</span></span> <span data-ttu-id="1fc61-117">Перехватываемые ошибка возникает при попытке присвоить новое значение в поле только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1fc61-117">A trappable error occurs if you try to assign a new value to a read-only field.</span></span>

<span data-ttu-id="1fc61-118">Обновляемый объект может содержать поля только для чтения, перед изменить запись проверьте свойство **DataUpdatable** каждое поле в коллекции **полей** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="1fc61-118">Because an updatable object can contain read-only fields, check the **DataUpdatable** property of each field in the **Fields** collection of a **Recordset** object before you edit a record.</span></span>

