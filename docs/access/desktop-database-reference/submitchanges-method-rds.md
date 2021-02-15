---
title: Метод SubmitChanges (RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ea7f3e27a75b4483cb8cf46e27d4492f831cff33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314401"
---
# <a name="submitchanges-method-rds"></a><span data-ttu-id="0c9d5-102">Метод SubmitChanges (RDS)</span><span class="sxs-lookup"><span data-stu-id="0c9d5-102">SubmitChanges method (RDS)</span></span>

<span data-ttu-id="0c9d5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c9d5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0c9d5-104">Отправка ожидающих изменений локально кэшируемых и updatable [recordset](recordset-object-ado.md) в источник данных, указанный в свойстве [Connect](connect-property-rds.md) или [URL-адресе.](url-property-rds.md)</span><span class="sxs-lookup"><span data-stu-id="0c9d5-104">Submits pending changes of the locally cached and updatable [Recordset](recordset-object-ado.md) to the data source specified in the [Connect](connect-property-rds.md) property or the [URL](url-property-rds.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c9d5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c9d5-105">Syntax</span></span>

<span data-ttu-id="0c9d5-106">*DataControl*. SubmitChanges</span><span class="sxs-lookup"><span data-stu-id="0c9d5-106">*DataControl*.SubmitChanges</span></span>

<span data-ttu-id="0c9d5-107">*DataFactory*. Подключение SubmitChanges, *Recordset*</span><span class="sxs-lookup"><span data-stu-id="0c9d5-107">*DataFactory*.SubmitChanges *Connection*, *Recordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="0c9d5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c9d5-108">Parameters</span></span>

|<span data-ttu-id="0c9d5-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="0c9d5-109">Parameter</span></span>|<span data-ttu-id="0c9d5-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0c9d5-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0c9d5-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="0c9d5-111">*DataControl*</span></span> |<span data-ttu-id="0c9d5-112">Объектная переменная, представляюная [RDS. Объект DataControl.](datacontrol-object-rds.md)</span><span class="sxs-lookup"><span data-stu-id="0c9d5-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="0c9d5-113">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="0c9d5-113">*DataFactory*</span></span> |<span data-ttu-id="0c9d5-114">Объектная переменная, представляюная [объект RDSServer.DataFactory.](datafactory-object-rdsserver.md)</span><span class="sxs-lookup"><span data-stu-id="0c9d5-114">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="0c9d5-115">*Connection*</span><span class="sxs-lookup"><span data-stu-id="0c9d5-115">*Connection*</span></span> |<span data-ttu-id="0c9d5-116">**Строка,** представляютив подключение, созданное с **помощью RDS. Свойство Connect объекта DataControl.** </span><span class="sxs-lookup"><span data-stu-id="0c9d5-116">A **String** value that represents the connection created with the **RDS.DataControl** object's **Connect** property.</span></span>|
|<span data-ttu-id="0c9d5-117">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="0c9d5-117">*Recordset*</span></span> |<span data-ttu-id="0c9d5-118">Объектная переменная, представляюная объект **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="0c9d5-118">An object variable that represents a **Recordset** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="0c9d5-119">Заметки</span><span class="sxs-lookup"><span data-stu-id="0c9d5-119">Remarks</span></span>

<span data-ttu-id="0c9d5-120">Свойства [Connect,](connect-property-rds.md) [Server](server-property-rds.md) [и SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) должны быть заданы перед использованием метода **SubmitChanges** с **RDS. Объект DataControl.**</span><span class="sxs-lookup"><span data-stu-id="0c9d5-120">The [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) properties must be set before you can use the **SubmitChanges** method with the **RDS.DataControl** object.</span></span>

<span data-ttu-id="0c9d5-121">Если вызвать метод [CancelUpdate](cancelupdate-method-rds.md) после вызова **SubmitChanges** для того же объекта **Recordset,** вызов **CancelUpdate** не удастся, так как изменения уже были зафиксированы.</span><span class="sxs-lookup"><span data-stu-id="0c9d5-121">If you call the [CancelUpdate](cancelupdate-method-rds.md) method after you have called **SubmitChanges** for the same **Recordset** object, the **CancelUpdate** call fails because the changes have already been committed.</span></span>

<span data-ttu-id="0c9d5-122">Для изменения отправляются только измененные записи, и либо все изменения будут успешными, либо все они будут сбой вместе.</span><span class="sxs-lookup"><span data-stu-id="0c9d5-122">Only the changed records are sent for modification, and either all of the changes succeed or all of them fail together.</span></span>

<span data-ttu-id="0c9d5-123">**SubmitChanges можно использовать** только с *объектом* **RDSServer.DataFactory** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0c9d5-123">You can use **SubmitChanges** only with the *default* **RDSServer.DataFactory** object.</span></span> <span data-ttu-id="0c9d5-124">Настраиваемые бизнес-объекты не могут использовать этот метод.</span><span class="sxs-lookup"><span data-stu-id="0c9d5-124">Custom business objects can't use this method.</span></span>

<span data-ttu-id="0c9d5-125">Если свойство **URL-адреса** задано, **SubmitChanges** будет отправлять изменения в расположение, указанное URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="0c9d5-125">If the **URL** property has been set, **SubmitChanges** will submit changes to the location specified by the URL.</span></span>

