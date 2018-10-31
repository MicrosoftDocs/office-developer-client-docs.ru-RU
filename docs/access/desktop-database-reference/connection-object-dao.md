---
title: Connection Object (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a8f324d7216eff2aeeb9045f5c506cdf37170f6
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863733"
---
# <a name="connection-object-dao"></a><span data-ttu-id="a2139-102">Connection Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="a2139-102">Connection Object (DAO)</span></span>


<span data-ttu-id="a2139-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a2139-103">**Applies to**: Access 2013 | Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="a2139-104">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="a2139-104">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="a2139-105">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a2139-105">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>



<span data-ttu-id="a2139-106">Объект **подключения** представляет подключение к базе данных ODBC (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="a2139-106">A **Connection** object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="a2139-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="a2139-107">Remarks</span></span>

<span data-ttu-id="a2139-108">**Подключение** — это непостоянные объект, представляющий подключение к удаленной базе данных.</span><span class="sxs-lookup"><span data-stu-id="a2139-108">A **Connection** is a non-persistent object that represents a connection to a remote database.</span></span> <span data-ttu-id="a2139-109">Объект **подключения** доступен только в рабочие области технология ODBCDirect (то есть, **рабочей области** объект, созданных с помощью параметра типа **dbUseODBC**).</span><span class="sxs-lookup"><span data-stu-id="a2139-109">The **Connection** object is only available in ODBCDirect workspaces (that is, a **Workspace** object created with the type option set to **dbUseODBC**).</span></span>


> [!NOTE]
> <span data-ttu-id="a2139-110">Код, написанный для более ранних версий DAO можно продолжить использование объекта **базы данных** для обеспечения обратной совместимости, но при желании новые возможности **подключения** , необходимо проверить код, чтобы использовать объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="a2139-110">Code written for earlier versions of DAO can continue to use the **Database** object for backward compatibility, but if the new features of a **Connection** are desired, you should revise code to use the **Connection** object.</span></span> <span data-ttu-id="a2139-111">Чтобы упростить преобразование кода, можно получить ссылку на объект **подключения** из **базы данных** , прочитав статью свойство [Connection](database-connection-property-dao.md) объекта **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="a2139-111">To help with code conversion, you can obtain a **Connection** object reference from a **Database** by reading the [Connection](database-connection-property-dao.md) property of the **Database** object.</span></span> <span data-ttu-id="a2139-112">С другой стороны можно получить ссылку на объект **базы данных** из свойства объекта **подключения к** **базе данных** .</span><span class="sxs-lookup"><span data-stu-id="a2139-112">Conversely, you can obtain a **Database** object reference from the **Connection** object's **Database** property.</span></span>


