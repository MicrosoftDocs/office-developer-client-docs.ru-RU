---
title: Метод TableDefs.Refresh (DAO)
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
# <a name="tabledefsrefresh-method-dao"></a><span data-ttu-id="2fde8-102">Метод TableDefs.Refresh (DAO)</span><span class="sxs-lookup"><span data-stu-id="2fde8-102">TableDefs.Refresh method (DAO)</span></span>


<span data-ttu-id="2fde8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2fde8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2fde8-104">Обновляет объекты в указанном уровне, чтобы отразить текущую схему базы данных.</span><span class="sxs-lookup"><span data-stu-id="2fde8-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fde8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2fde8-105">Syntax</span></span>

<span data-ttu-id="2fde8-106">*выражение .* Обновление</span><span class="sxs-lookup"><span data-stu-id="2fde8-106">*expression* .Refresh</span></span>

<span data-ttu-id="2fde8-107">*выражение* Переменная, представляюная объект **TableDefs.**</span><span class="sxs-lookup"><span data-stu-id="2fde8-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fde8-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="2fde8-108">Remarks</span></span>

<span data-ttu-id="2fde8-109">Чтобы определить позицию, используемую ядром базы данных Microsoft Access для объектов **Field** в коллекции **Fields** объекта **QueryDef,** **Recordset** или **TableDef,** используйте свойство **OrdinalPosition** каждого объекта **Field.**</span><span class="sxs-lookup"><span data-stu-id="2fde8-109">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object.</span></span> <span data-ttu-id="2fde8-110">Изменение свойства **OrdinalPosition** объекта **Field** может не изменять порядок объектов **Field** в коллекции, пока не будет применяться метод **Refresh.**</span><span class="sxs-lookup"><span data-stu-id="2fde8-110">Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="2fde8-111">Используйте метод **Refresh** в многомерных средах, в которых другие пользователи могут изменить базу данных.</span><span class="sxs-lookup"><span data-stu-id="2fde8-111">Use the **Refresh** method in multiuser environments in which other users may change the database.</span></span> <span data-ttu-id="2fde8-112">Кроме того, может потребоваться использовать его в любых коллекциях, на которые косвенно влияют изменения базы данных.</span><span class="sxs-lookup"><span data-stu-id="2fde8-112">You may also need to use it on any collections that are indirectly affected by changes to the database.</span></span> <span data-ttu-id="2fde8-113">Например, при изменении коллекции **Users** может потребоваться обновить коллекцию **Groups** перед ее **использованием.**</span><span class="sxs-lookup"><span data-stu-id="2fde8-113">For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="2fde8-114">Коллекция заполняется объектами при первом ссылке и не отражает автоматически последующие изменения, внесенные другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="2fde8-114">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make.</span></span> <span data-ttu-id="2fde8-115">Если, скорее всего, другой пользователь изменил коллекцию, используйте метод Refresh в коллекции непосредственно перед тем, как выполнять любую задачу в приложении, предполагая наличие или отсутствие определенного объекта в коллекции.</span><span class="sxs-lookup"><span data-stu-id="2fde8-115">If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection.</span></span> <span data-ttu-id="2fde8-116">Это гарантирует, что коллекция будет как можно более новой.</span><span class="sxs-lookup"><span data-stu-id="2fde8-116">This will ensure that the collection is as up-to-date as possible.</span></span> <span data-ttu-id="2fde8-117">С другой стороны, использование refresh может привести к излишнему замедлению производительности.</span><span class="sxs-lookup"><span data-stu-id="2fde8-117">On the other hand, using Refresh can unnecessarily slow performance.</span></span>

