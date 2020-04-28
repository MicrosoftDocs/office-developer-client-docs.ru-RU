---
title: Метод Refresh (RDS)
TOCTitle: Refresh method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 60de3b25e5eedc277eaafbe4bd1c078863e13f7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309301"
---
# <a name="refresh-method-rds"></a><span data-ttu-id="a1809-102">Метод Refresh (RDS)</span><span class="sxs-lookup"><span data-stu-id="a1809-102">Refresh method (RDS)</span></span>

<span data-ttu-id="a1809-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1809-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1809-104">Повторно запрашивает источник данных, указанный в свойстве [Connect](connect-property-rds.md) , и обновляет результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="a1809-104">Requeries the data source specified in the [Connect](connect-property-rds.md) property and updates the query results.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1809-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1809-105">Syntax</span></span>

<span data-ttu-id="a1809-106">*Элемент управления*. Обновление</span><span class="sxs-lookup"><span data-stu-id="a1809-106">*DataControl*.Refresh</span></span>

## <a name="parameters"></a><span data-ttu-id="a1809-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1809-107">Parameters</span></span>

|<span data-ttu-id="a1809-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="a1809-108">Parameter</span></span>|<span data-ttu-id="a1809-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a1809-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a1809-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="a1809-110">*DataControl*</span></span> |<span data-ttu-id="a1809-111">Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.</span><span class="sxs-lookup"><span data-stu-id="a1809-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a1809-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="a1809-112">Remarks</span></span>

<span data-ttu-id="a1809-113">Прежде чем использовать метод **Refresh** , необходимо задать свойства [Connect](connect-property-rds.md), [Server](server-property-rds.md)и [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) .</span><span class="sxs-lookup"><span data-stu-id="a1809-113">You must set the [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) properties before you use the **Refresh** method.</span></span> <span data-ttu-id="a1809-114">Все элементы управления с привязкой к данным в форме, связанной с **RDS. Объект элемента управления** данным будет отражать новый набор записей.</span><span class="sxs-lookup"><span data-stu-id="a1809-114">All data-bound controls on the form associated with an **RDS.DataControl** object will reflect the new set of records.</span></span> <span data-ttu-id="a1809-115">Освобождается любой существующий объект [Recordset](recordset-object-ado.md) , а все несохраненные изменения отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="a1809-115">Any pre-existing [Recordset](recordset-object-ado.md) object is released, and any unsaved changes are discarded.</span></span> <span data-ttu-id="a1809-116">Метод **Refresh** автоматически создает первую запись в текущей записи.</span><span class="sxs-lookup"><span data-stu-id="a1809-116">The **Refresh** method automatically makes the first record the current record.</span></span>

<span data-ttu-id="a1809-117">Рекомендуется периодически вызывать метод **Refresh** при работе с данными.</span><span class="sxs-lookup"><span data-stu-id="a1809-117">It's a good idea to call the **Refresh** method periodically when you work with data.</span></span> <span data-ttu-id="a1809-118">Если получить данные, а затем оставить их на клиентском компьютере в течение этого времени, скорее всего, оно станет устаревшим.</span><span class="sxs-lookup"><span data-stu-id="a1809-118">If you retrieve data, and then leave it on your client machine for a while, it is likely to become out of date.</span></span> <span data-ttu-id="a1809-119">Возможно, все внесенные изменения не будут выполнены, так как другой пользователь изменил запись и отправил изменения.</span><span class="sxs-lookup"><span data-stu-id="a1809-119">It's possible that any changes you make will fail, because someone else might have changed the record and submitted changes before you.</span></span>

