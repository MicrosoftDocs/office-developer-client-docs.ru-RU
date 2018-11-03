---
title: Метод TableDefs.Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: f76c1a3f-1561-ce1f-a535-a5a2179ea739
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836915(v=office.15)
ms:contentKeyID: 48548765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 53a632999f1b60b078e9365c9f99e52ddec284e9
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927881"
---
# <a name="tabledefsrefresh-method-dao"></a><span data-ttu-id="1d734-102">Метод TableDefs.Refresh (DAO)</span><span class="sxs-lookup"><span data-stu-id="1d734-102">TableDefs.Refresh method (DAO)</span></span>


<span data-ttu-id="1d734-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d734-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d734-104">Обновляет объекты в указанном включающий в соответствии с текущей схеме базы данных.</span><span class="sxs-lookup"><span data-stu-id="1d734-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d734-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d734-105">Syntax</span></span>

<span data-ttu-id="1d734-106">*выражение* . Обновление</span><span class="sxs-lookup"><span data-stu-id="1d734-106">*expression* .Refresh</span></span>

<span data-ttu-id="1d734-107">*выражение* Переменная, которая представляет собой объект- **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="1d734-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d734-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="1d734-108">Remarks</span></span>

<span data-ttu-id="1d734-109">Чтобы определить позицию, ядро базы данных Microsoft Access с помощью **поля** объектов в коллекции **полей** **QueryDef**, **набора записей**или **TableDef** объекта, используйте свойство **OrdinalPosition** Каждый объект **поля** .</span><span class="sxs-lookup"><span data-stu-id="1d734-109">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object.</span></span> <span data-ttu-id="1d734-110">Изменение свойства **OrdinalPosition** объекта **поля** могут не изменить порядок **полей** объектов в коллекции только при вызове метода **обновления на**</span><span class="sxs-lookup"><span data-stu-id="1d734-110">Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="1d734-111">Используйте метод **Refresh** в многопользовательских средах, в которых другие пользователи могут изменить базу данных.</span><span class="sxs-lookup"><span data-stu-id="1d734-111">Use the **Refresh** method in multiuser environments in which other users may change the database.</span></span> <span data-ttu-id="1d734-112">Кроме того, может потребоваться использовать на всех коллекций, которые косвенно затронуты изменениями в базе данных.</span><span class="sxs-lookup"><span data-stu-id="1d734-112">You may also need to use it on any collections that are indirectly affected by changes to the database.</span></span> <span data-ttu-id="1d734-113">Например при изменении коллекции **пользователей** может потребоваться обновить коллекцию **групп** перед использованием семейства сайтов **групп** .</span><span class="sxs-lookup"><span data-stu-id="1d734-113">For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="1d734-114">Объекты в первый раз оно используется для ссылки и не отражает изменения, которые другие пользователи автоматически заполняется коллекцию.</span><span class="sxs-lookup"><span data-stu-id="1d734-114">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make.</span></span> <span data-ttu-id="1d734-115">Если это скорее всего, что другой пользователь был изменен коллекцию, используйте метод Refresh в семействе сайтов непосредственно перед выполнению любой из задач в приложения, которые предполагается наличие или отсутствие определенного объекта в коллекции.</span><span class="sxs-lookup"><span data-stu-id="1d734-115">If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection.</span></span> <span data-ttu-id="1d734-116">Это гарантирует, что коллекции с самым последним обновлением.</span><span class="sxs-lookup"><span data-stu-id="1d734-116">This will ensure that the collection is as up-to-date as possible.</span></span> <span data-ttu-id="1d734-117">С другой стороны с помощью обновления без необходимости может снизить производительность.</span><span class="sxs-lookup"><span data-stu-id="1d734-117">On the other hand, using Refresh can unnecessarily slow performance.</span></span>

