---
title: Database.Connection Property (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7f0974051b1f10fa73caad6d9feafb2e2b769579
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882842"
---
# <a name="databaseconnection-property-dao"></a><span data-ttu-id="66cf7-102">Database.Connection Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="66cf7-102">Database.Connection Property (DAO)</span></span>


<span data-ttu-id="66cf7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66cf7-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="66cf7-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66cf7-104">Syntax</span></span>

<span data-ttu-id="66cf7-105">*выражение* . Подключение</span><span class="sxs-lookup"><span data-stu-id="66cf7-105">*expression* .Connection</span></span>

<span data-ttu-id="66cf7-106">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="66cf7-106">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="66cf7-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="66cf7-107">Remarks</span></span>

<span data-ttu-id="66cf7-108">Используйте свойство **подключение** для получения ссылки на объект **подключения** , соответствующее **базы данных**.</span><span class="sxs-lookup"><span data-stu-id="66cf7-108">Use the **Connection** property to obtain a reference to a **Connection** object that corresponds to the **Database**.</span></span> <span data-ttu-id="66cf7-109">В DAO, объект **подключения** и его соответствующего объекта **базы данных** — это просто два разных объектных переменных ссылки на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="66cf7-109">In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object.</span></span> <span data-ttu-id="66cf7-110">**[База данных](connection-database-property-dao.md)** свойств объекта **подключения** и свойство **Connection** объекта **базы данных** облегчают изменять подключения к источнику данных ODBC с помощью ядро базы данных Microsoft Access, чтобы использовать технология ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="66cf7-110">The **[Database](connection-database-property-dao.md)** property of a **Connection** object and the **Connection** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

