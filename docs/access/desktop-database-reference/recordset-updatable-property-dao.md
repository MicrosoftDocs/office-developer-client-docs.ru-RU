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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307548"
---
# <a name="recordsetupdatable-property-dao"></a><span data-ttu-id="7424e-102">Свойство Recordset.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="7424e-102">Recordset.Updatable property (DAO)</span></span>


<span data-ttu-id="7424e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7424e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7424e-104">Возвращает значение, которое указывает на то, можно ли изменить DAO объект.</span><span class="sxs-lookup"><span data-stu-id="7424e-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="7424e-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="7424e-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7424e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7424e-106">Syntax</span></span>

<span data-ttu-id="7424e-107">*выражения* . Updatable</span><span class="sxs-lookup"><span data-stu-id="7424e-107">*expression* .Updatable</span></span>

<span data-ttu-id="7424e-108">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="7424e-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7424e-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="7424e-109">Remarks</span></span>

<span data-ttu-id="7424e-110">Объекты Recordset с мгновенными снимками и только для форвардного типа всегда возвращают **false**.</span><span class="sxs-lookup"><span data-stu-id="7424e-110">Snapshot- and forward-only–type Recordset objects always return **False**.</span></span>

<span data-ttu-id="7424e-111">Многие типы объектов могут содержать поля, которые не могут быть обновлены.</span><span class="sxs-lookup"><span data-stu-id="7424e-111">Many types of objects can contain fields that can't be updated.</span></span> <span data-ttu-id="7424e-112">Например, можно создать объект **Recordset** типа dynaset, в котором можно изменить только некоторые поля.</span><span class="sxs-lookup"><span data-stu-id="7424e-112">For example, you can create a dynaset-type **Recordset** object in which only some fields can be changed.</span></span> <span data-ttu-id="7424e-113">Эти поля могут быть исправлены или содержать данные, которые автоматически прибавления, или dynaset может быть результатом запроса, который объединяет updatable и nonupdatable таблицы.</span><span class="sxs-lookup"><span data-stu-id="7424e-113">These fields can be fixed or contain data that increments automatically, or the dynaset can result from a query that combines updatable and nonupdatable tables.</span></span>

<span data-ttu-id="7424e-114">Если объект содержит только поля только для чтения, значение свойства **Updatable** **false**.</span><span class="sxs-lookup"><span data-stu-id="7424e-114">If the object contains only read-only fields, the value of the **Updatable** property is **False**.</span></span> <span data-ttu-id="7424e-115">Если одно или несколько полей являются updatable, значение свойства **True**.</span><span class="sxs-lookup"><span data-stu-id="7424e-115">When one or more fields are updatable, the property's value is **True**.</span></span> <span data-ttu-id="7424e-116">Можно редактировать только updatable fields.</span><span class="sxs-lookup"><span data-stu-id="7424e-116">You can edit only the updatable fields.</span></span> <span data-ttu-id="7424e-117">При попытке назначить новое значение в поле только для чтения возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="7424e-117">A trappable error occurs if you try to assign a new value to a read-only field.</span></span>

<span data-ttu-id="7424e-118">Так как updatable объект может содержать поля только для чтения, перед редактированием записи проверьте свойство **DataUpdatable** для каждого поля в коллекции **Полей** объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="7424e-118">Because an updatable object can contain read-only fields, check the **DataUpdatable** property of each field in the **Fields** collection of a **Recordset** object before you edit a record.</span></span>

