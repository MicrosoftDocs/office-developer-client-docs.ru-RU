---
title: Методы TableDef. Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: f76c1a3f-1561-ce1f-a535-a5a2179ea739
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836915(v=office.15)
ms:contentKeyID: 48548765
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6050e2d0b97421bda7a2914f068db4019459ee7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306316"
---
# <a name="tabledefsrefresh-method-dao"></a><span data-ttu-id="8afbf-102">Методы TableDef. Refresh (DAO)</span><span class="sxs-lookup"><span data-stu-id="8afbf-102">TableDefs.Refresh method (DAO)</span></span>


<span data-ttu-id="8afbf-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8afbf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8afbf-104">Обновляет объекты в заданном коллетион в соответствии с текущей схемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="8afbf-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="8afbf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8afbf-105">Syntax</span></span>

<span data-ttu-id="8afbf-106">*Expression* . Обновление</span><span class="sxs-lookup"><span data-stu-id="8afbf-106">*expression* .Refresh</span></span>

<span data-ttu-id="8afbf-107">*Expression (выражение* ) Переменная, представляющая объект **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="8afbf-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8afbf-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="8afbf-108">Remarks</span></span>

<span data-ttu-id="8afbf-109">Чтобы определить положение, которое ядро СУБД Microsoft Access использует для объектов **field** в коллекции **Fields** объекта **QueryDef**, **Recordset**или **tabledef** , используйте свойство **ординалпоситион** объекта каждого объекта **field** .</span><span class="sxs-lookup"><span data-stu-id="8afbf-109">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object.</span></span> <span data-ttu-id="8afbf-110">Изменение свойства **ординалпоситион** объекта **field** не приводит к изменению порядка объектов **field** в коллекции до тех пор, пока не будет использован метод **Refresh** .</span><span class="sxs-lookup"><span data-stu-id="8afbf-110">Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="8afbf-111">Используйте метод **Refresh** в многопользовательской среде, в которой другие пользователи могут изменить базу данных.</span><span class="sxs-lookup"><span data-stu-id="8afbf-111">Use the **Refresh** method in multiuser environments in which other users may change the database.</span></span> <span data-ttu-id="8afbf-112">Его также можно использовать для всех коллекций, на которые косвенно влияют изменения базы данных.</span><span class="sxs-lookup"><span data-stu-id="8afbf-112">You may also need to use it on any collections that are indirectly affected by changes to the database.</span></span> <span data-ttu-id="8afbf-113">Например, если вы измените коллекцию **пользователей** , вам может потребоваться обновить коллекцию **Groups** перед использованием коллекции **Groups** .</span><span class="sxs-lookup"><span data-stu-id="8afbf-113">For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="8afbf-114">Коллекция заполняется объектами, на которые она выполняется при первом запуске, и не автоматически отражает последующие изменения, внесенные другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="8afbf-114">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make.</span></span> <span data-ttu-id="8afbf-115">Если, вероятно, другой пользователь изменил коллекцию, используйте метод Refresh в коллекции сразу же перед выполнением любой задачи в приложении, которая предполагает присутствие или отсутствие определенного объекта в коллекции.</span><span class="sxs-lookup"><span data-stu-id="8afbf-115">If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection.</span></span> <span data-ttu-id="8afbf-116">Это гарантирует, что коллекция будет как можно более актуальной.</span><span class="sxs-lookup"><span data-stu-id="8afbf-116">This will ensure that the collection is as up-to-date as possible.</span></span> <span data-ttu-id="8afbf-117">С другой стороны, использование функции обновления может снизить производительность.</span><span class="sxs-lookup"><span data-stu-id="8afbf-117">On the other hand, using Refresh can unnecessarily slow performance.</span></span>

