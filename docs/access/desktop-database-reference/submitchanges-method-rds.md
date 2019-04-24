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
# <a name="submitchanges-method-rds"></a><span data-ttu-id="d2108-102">Метод SubmitChanges (RDS)</span><span class="sxs-lookup"><span data-stu-id="d2108-102">SubmitChanges method (RDS)</span></span>

<span data-ttu-id="d2108-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2108-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2108-104">Передает ожидающие изменения локального кэшированного и обновляемого [набора записей](recordset-object-ado.md) в источник данных, указанный в свойстве [Connect](connect-property-rds.md) или [URL-адрес](url-property-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="d2108-104">Submits pending changes of the locally cached and updatable [Recordset](recordset-object-ado.md) to the data source specified in the [Connect](connect-property-rds.md) property or the [URL](url-property-rds.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2108-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2108-105">Syntax</span></span>

<span data-ttu-id="d2108-106">*Элемент управления*. SubmitChanges</span><span class="sxs-lookup"><span data-stu-id="d2108-106">*DataControl*.SubmitChanges</span></span>

<span data-ttu-id="d2108-107">*Фактическое*. *Подключение*SubmitChanges, *набор записей*</span><span class="sxs-lookup"><span data-stu-id="d2108-107">*DataFactory*.SubmitChanges*Connection*, *Recordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="d2108-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2108-108">Parameters</span></span>

|<span data-ttu-id="d2108-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="d2108-109">Parameter</span></span>|<span data-ttu-id="d2108-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d2108-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d2108-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="d2108-111">*DataControl*</span></span> |<span data-ttu-id="d2108-112">Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.</span><span class="sxs-lookup"><span data-stu-id="d2108-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="d2108-113">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="d2108-113">*DataFactory*</span></span> |<span data-ttu-id="d2108-114">Объектная переменная, представляющая объект [фактОв рдссервер.](datafactory-object-rdsserver.md) DataObject.</span><span class="sxs-lookup"><span data-stu-id="d2108-114">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="d2108-115">*Connection*</span><span class="sxs-lookup"><span data-stu-id="d2108-115">*Connection*</span></span> |<span data-ttu-id="d2108-116">**Строковое** значение, представляющее подключение, созданное с помощью \*\*RDS. \*\*Свойство **Connect** объекта DataObject.</span><span class="sxs-lookup"><span data-stu-id="d2108-116">A **String** value that represents the connection created with the **RDS.DataControl** object's **Connect** property.</span></span>|
|<span data-ttu-id="d2108-117">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="d2108-117">*Recordset*</span></span> |<span data-ttu-id="d2108-118">Объектная переменная, представляющая объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="d2108-118">An object variable that represents a **Recordset** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d2108-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="d2108-119">Remarks</span></span>

<span data-ttu-id="d2108-120">Необходимо задать свойства [Connect](connect-property-rds.md), [Server](server-property-rds.md)и [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) , прежде чем можно будет использовать метод **SubmitChanges** с помощью **RDS. Объект управления** DataObject.</span><span class="sxs-lookup"><span data-stu-id="d2108-120">The [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) properties must be set before you can use the **SubmitChanges** method with the **RDS.DataControl** object.</span></span>

<span data-ttu-id="d2108-121">Если метод [CancelUpdate](cancelupdate-method-rds.md) вызывается после вызова **SubmitChanges** для того же объекта **Recordset** , вызов **CancelUpdate** завершится с ошибкой, так как изменения уже были зафиксированы.</span><span class="sxs-lookup"><span data-stu-id="d2108-121">If you call the [CancelUpdate](cancelupdate-method-rds.md) method after you have called **SubmitChanges** for the same **Recordset** object, the **CancelUpdate** call fails because the changes have already been committed.</span></span>

<span data-ttu-id="d2108-122">Только измененные записи отправляются для изменения и либо все изменения успешно выполнены, либо все они работают вместе.</span><span class="sxs-lookup"><span data-stu-id="d2108-122">Only the changed records are sent for modification, and either all of the changes succeed or all of them fail together.</span></span>

<span data-ttu-id="d2108-123">Параметр **SubmitChanges** можно использовать только с объектом **рдссервер.** DataObject, *используемым по умолчанию* .</span><span class="sxs-lookup"><span data-stu-id="d2108-123">You can use **SubmitChanges** only with the *default* **RDSServer.DataFactory** object.</span></span> <span data-ttu-id="d2108-124">Пользовательские бизнес-объекты не могут использовать этот метод.</span><span class="sxs-lookup"><span data-stu-id="d2108-124">Custom business objects can't use this method.</span></span>

<span data-ttu-id="d2108-125">Если задано свойство **URL** , **SubmitChanges** отправит изменения в расположении, указанном с помощью URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="d2108-125">If the **URL** property has been set, **SubmitChanges** will submit changes to the location specified by the URL.</span></span>

