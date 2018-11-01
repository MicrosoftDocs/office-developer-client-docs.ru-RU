---
title: Recordset2.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: ad8184b6-ffe3-dde6-ddee-4b23cdaa9c59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821726(v=office.15)
ms:contentKeyID: 48547041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba986d76126b6e805b8bf7a52299cfc16f5841d8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881638"
---
# <a name="recordset2updatable-property-dao"></a><span data-ttu-id="04c76-102">Recordset2.Updatable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="04c76-102">Recordset2.Updatable Property (DAO)</span></span>


<span data-ttu-id="04c76-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="04c76-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04c76-104">Возвращает значение, указывающее, является ли объект DAO можно изменить.</span><span class="sxs-lookup"><span data-stu-id="04c76-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="04c76-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="04c76-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="04c76-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04c76-106">Syntax</span></span>

<span data-ttu-id="04c76-107">*выражение* . Обновляемые</span><span class="sxs-lookup"><span data-stu-id="04c76-107">*expression* .Updatable</span></span>

<span data-ttu-id="04c76-108">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="04c76-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="04c76-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="04c76-109">Remarks</span></span>

<span data-ttu-id="04c76-110">Моментальный снимок и прямого только – набора записей объекты типа всегда возвращает **значение False**.</span><span class="sxs-lookup"><span data-stu-id="04c76-110">Snapshot- and forward-only–type Recordset objects always return **False**.</span></span>

<span data-ttu-id="04c76-111">Несколько типов объектов может содержать поля, которые не могут быть обновлены.</span><span class="sxs-lookup"><span data-stu-id="04c76-111">Many types of objects can contain fields that can't be updated.</span></span> <span data-ttu-id="04c76-112">Например можно создать объект типа динамического **набора записей** , в котором можно изменить только некоторые поля.</span><span class="sxs-lookup"><span data-stu-id="04c76-112">For example, you can create a dynaset-type **Recordset** object in which only some fields can be changed.</span></span> <span data-ttu-id="04c76-113">Эти поля устранения или содержат данные, автоматически увеличивает или динамический набор может привести к из запроса, который объединяет обновляемых и nonupdatable таблицы.</span><span class="sxs-lookup"><span data-stu-id="04c76-113">These fields can be fixed or contain data that increments automatically, or the dynaset can result from a query that combines updatable and nonupdatable tables.</span></span>

<span data-ttu-id="04c76-114">Если объект содержит поля только для чтения, значение свойства **с возможностью записи** имеет **значение False**.</span><span class="sxs-lookup"><span data-stu-id="04c76-114">If the object contains only read-only fields, the value of the **Updatable** property is **False**.</span></span> <span data-ttu-id="04c76-115">Когда обновляемых одно или несколько полей, значение свойства — **True**.</span><span class="sxs-lookup"><span data-stu-id="04c76-115">When one or more fields are updatable, the property's value is **True**.</span></span> <span data-ttu-id="04c76-116">Можно изменить только обновляемых полей.</span><span class="sxs-lookup"><span data-stu-id="04c76-116">You can edit only the updatable fields.</span></span> <span data-ttu-id="04c76-117">Перехватываемые ошибка возникает при попытке присвоить новое значение в поле только для чтения.</span><span class="sxs-lookup"><span data-stu-id="04c76-117">A trappable error occurs if you try to assign a new value to a read-only field.</span></span>

<span data-ttu-id="04c76-118">Обновляемый объект может содержать поля только для чтения, перед изменить запись проверьте свойство **DataUpdatable** каждое поле в коллекции **полей** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="04c76-118">Because an updatable object can contain read-only fields, check the **DataUpdatable** property of each field in the **Fields** collection of a **Recordset** object before you edit a record.</span></span>

