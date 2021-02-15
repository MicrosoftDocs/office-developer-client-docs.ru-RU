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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309326"
---
# <a name="recordset2updatable-property-dao"></a><span data-ttu-id="f1b44-102">Свойство Recordset2.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="f1b44-102">Recordset2.Updatable property (DAO)</span></span>


<span data-ttu-id="f1b44-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f1b44-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f1b44-104">Возвращает значение, которое указывает на то, можно ли изменить DAO объект.</span><span class="sxs-lookup"><span data-stu-id="f1b44-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="f1b44-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1b44-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1b44-106">Syntax</span></span>

<span data-ttu-id="f1b44-107">*выражение .* Updatable</span><span class="sxs-lookup"><span data-stu-id="f1b44-107">*expression* .Updatable</span></span>

<span data-ttu-id="f1b44-108">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="f1b44-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1b44-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="f1b44-109">Remarks</span></span>

<span data-ttu-id="f1b44-110">Объекты Recordset типа "моментальный снимок" и "только для переад/ всегда возвращают **false.**</span><span class="sxs-lookup"><span data-stu-id="f1b44-110">Snapshot- and forward-only–type Recordset objects always return **False**.</span></span>

<span data-ttu-id="f1b44-111">Многие типы объектов могут содержать поля, которые не могут быть обновлены.</span><span class="sxs-lookup"><span data-stu-id="f1b44-111">Many types of objects can contain fields that can't be updated.</span></span> <span data-ttu-id="f1b44-112">Например, можно создать объект **Recordset** типа dynaset, в котором можно изменить только некоторые поля.</span><span class="sxs-lookup"><span data-stu-id="f1b44-112">For example, you can create a dynaset-type **Recordset** object in which only some fields can be changed.</span></span> <span data-ttu-id="f1b44-113">Эти поля могут быть исправлены или содержать данные, которые автоматически приращены, или набор dynaset может быть результатом запроса, объединяющего неустанные и неустандартные таблицы.</span><span class="sxs-lookup"><span data-stu-id="f1b44-113">These fields can be fixed or contain data that increments automatically, or the dynaset can result from a query that combines updatable and nonupdatable tables.</span></span>

<span data-ttu-id="f1b44-114">Если объект содержит только поля только для чтения, свойство **Updatable** имеет значение **False.**</span><span class="sxs-lookup"><span data-stu-id="f1b44-114">If the object contains only read-only fields, the value of the **Updatable** property is **False**.</span></span> <span data-ttu-id="f1b44-115">Если одно или несколько полей могут быть updatable, свойство имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="f1b44-115">When one or more fields are updatable, the property's value is **True**.</span></span> <span data-ttu-id="f1b44-116">Можно редактировать только поля, которые можно изменить.</span><span class="sxs-lookup"><span data-stu-id="f1b44-116">You can edit only the updatable fields.</span></span> <span data-ttu-id="f1b44-117">Если попытаться назначить новое значение только для чтения, возникает перехитиемая ошибка.</span><span class="sxs-lookup"><span data-stu-id="f1b44-117">A trappable error occurs if you try to assign a new value to a read-only field.</span></span>

<span data-ttu-id="f1b44-118">Так как updatable объект может содержать поля только для чтения, перед редактированием записи проверьте свойство **DataUpdatable** каждого поля в коллекции **Fields** объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="f1b44-118">Because an updatable object can contain read-only fields, check the **DataUpdatable** property of each field in the **Fields** collection of a **Recordset** object before you edit a record.</span></span>

