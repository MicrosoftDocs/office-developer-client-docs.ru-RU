---
title: Метод SubmitChanges (RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 92634f2c0d95fbe9022934d22340f768b5614a58
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923373"
---
# <a name="submitchanges-method-rds"></a><span data-ttu-id="0dd96-102">Метод SubmitChanges (RDS)</span><span class="sxs-lookup"><span data-stu-id="0dd96-102">SubmitChanges method (RDS)</span></span>


<span data-ttu-id="0dd96-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0dd96-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0dd96-104">Отправляет ожидающие изменения локально кэширования и обновляемых [записей](recordset-object-ado.md) в источник данных, указанный в свойстве [Connect](connect-property-rds.md) или свойстве [URL-адрес](url-property-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="0dd96-104">Submits pending changes of the locally cached and updatable [Recordset](recordset-object-ado.md) to the data source specified in the [Connect](connect-property-rds.md) property or the [URL](url-property-rds.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dd96-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0dd96-105">Syntax</span></span>

<span data-ttu-id="0dd96-106">*DataControl*. SubmitChanges</span><span class="sxs-lookup"><span data-stu-id="0dd96-106">*DataControl*.SubmitChanges</span></span>

<span data-ttu-id="0dd96-107">*DataFactory*. SubmitChanges*подключения*, *записей*</span><span class="sxs-lookup"><span data-stu-id="0dd96-107">*DataFactory*.SubmitChanges*Connection*, *Recordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="0dd96-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0dd96-108">Parameters</span></span>

  - <span data-ttu-id="0dd96-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="0dd96-109">*DataControl*</span></span>

  - <span data-ttu-id="0dd96-110">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="0dd96-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="0dd96-111">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="0dd96-111">*DataFactory*</span></span>

  - <span data-ttu-id="0dd96-112">Объектная переменная, которая представляет объект [RDSServer.DataFactory](datafactory-object-rdsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="0dd96-112">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>

  - <span data-ttu-id="0dd96-113">*Подключение*</span><span class="sxs-lookup"><span data-stu-id="0dd96-113">*Connection*</span></span>

  - <span data-ttu-id="0dd96-114">Значение типа **String** , представляющий подключение, созданных с помощью **RDS. DataControl** **Подключить** свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="0dd96-114">A **String** value that represents the connection created with the **RDS.DataControl** object's **Connect** property.</span></span>

  - <span data-ttu-id="0dd96-115">*Набор записей*</span><span class="sxs-lookup"><span data-stu-id="0dd96-115">*Recordset*</span></span>

  - <span data-ttu-id="0dd96-116">Объектная переменная, представляющий объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="0dd96-116">An object variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dd96-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="0dd96-117">Remarks</span></span>

<span data-ttu-id="0dd96-118">Необходимо задать свойства [подключения](connect-property-rds.md), [сервер](server-property-rds.md)и [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) , прежде чем использовать метод **SubmitChanges** с **RDS. DataControl** объекта.</span><span class="sxs-lookup"><span data-stu-id="0dd96-118">The [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) properties must be set before you can use the **SubmitChanges** method with the **RDS.DataControl** object.</span></span>

<span data-ttu-id="0dd96-119">При вызове метода [CancelUpdate](cancelupdate-method-rds.md) после вызова **SubmitChanges** для одного объекта **набора записей** , **CancelUpdate** завершается неудачно, так как эти изменения уже была выполнена.</span><span class="sxs-lookup"><span data-stu-id="0dd96-119">If you call the [CancelUpdate](cancelupdate-method-rds.md) method after you have called **SubmitChanges** for the same **Recordset** object, the **CancelUpdate** call fails because the changes have already been committed.</span></span>

<span data-ttu-id="0dd96-120">Измененные записи будут отправлены для изменения и всех изменений выполнен удачно или все из них нет друг с другом.</span><span class="sxs-lookup"><span data-stu-id="0dd96-120">Only the changed records are sent for modification, and either all of the changes succeed or all of them fail together.</span></span>

<span data-ttu-id="0dd96-121">**SubmitChanges** можно использовать только с помощью объекта **RDSServer.DataFactory** *по умолчанию* .</span><span class="sxs-lookup"><span data-stu-id="0dd96-121">You can use **SubmitChanges** only with the *default* **RDSServer.DataFactory** object.</span></span> <span data-ttu-id="0dd96-122">Этот способ нельзя использовать настраиваемые бизнес-объекты.</span><span class="sxs-lookup"><span data-stu-id="0dd96-122">Custom business objects can't use this method.</span></span>

<span data-ttu-id="0dd96-123">Если свойство **URL-адрес** **SubmitChanges** будет внесения изменений в расположении, указанном URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="0dd96-123">If the **URL** property has been set, **SubmitChanges** will submit changes to the location specified by the URL.</span></span>

