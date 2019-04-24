---
title: Объект Connection (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 73ede9cae5246db3d802125b0f7c4e6df5347930
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295865"
---
# <a name="connection-object-dao"></a><span data-ttu-id="56f25-102">Объект Connection (DAO)</span><span class="sxs-lookup"><span data-stu-id="56f25-102">Connection object (DAO)</span></span>

<span data-ttu-id="56f25-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="56f25-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="56f25-104">Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="56f25-104">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="56f25-105">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="56f25-105">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="56f25-106">Объект **Connection** представляет подключение к базе данных ODBC (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="56f25-106">A **Connection** object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="56f25-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="56f25-107">Remarks</span></span>

<span data-ttu-id="56f25-108">**Подключение** — это непостоянный объект, представляющий подключение к удаленной базе данных.</span><span class="sxs-lookup"><span data-stu-id="56f25-108">A **Connection** is a non-persistent object that represents a connection to a remote database.</span></span> <span data-ttu-id="56f25-109">Объект **Connection** доступен только в рабочих областях ODBCDirect (то есть объект **Workspace** , созданный с параметром Type, для которого установлено значение **дбусеодбк**).</span><span class="sxs-lookup"><span data-stu-id="56f25-109">The **Connection** object is only available in ODBCDirect workspaces (that is, a **Workspace** object created with the type option set to **dbUseODBC**).</span></span>

> [!NOTE]
> <span data-ttu-id="56f25-110">Код, написанный для более ранних версий DAO, может продолжать использовать объект **базы данных** для обратной совместимости, но если вам нужны новые возможности **подключения** , следует исправить код, чтобы использовать объект **Connection** .</span><span class="sxs-lookup"><span data-stu-id="56f25-110">Code written for earlier versions of DAO can continue to use the **Database** object for backward compatibility, but if the new features of a **Connection** are desired, you should revise code to use the **Connection** object.</span></span> <span data-ttu-id="56f25-111">Чтобы упростить преобразование кода, можно получить ссылку на объект **подключения** из **базы данных** , читая свойство [Connection](database-connection-property-dao.md) объекта **Database** .</span><span class="sxs-lookup"><span data-stu-id="56f25-111">To help with code conversion, you can obtain a **Connection** object reference from a **Database** by reading the [Connection](database-connection-property-dao.md) property of the **Database** object.</span></span> <span data-ttu-id="56f25-112">И наоборот, можно получить ссылку на объект **базы данных** из свойства **базы данных** объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="56f25-112">Conversely, you can obtain a **Database** object reference from the **Connection** object's **Database** property.</span></span>


