---
title: Обновления метода (RDS)
TOCTitle: Refresh Method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bccb7c14b5b8666a5058ad8de489ef248f39ddda
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868632"
---
# <a name="refresh-method-rds"></a><span data-ttu-id="3c51a-102">Обновления метода (RDS)</span><span class="sxs-lookup"><span data-stu-id="3c51a-102">Refresh Method (RDS)</span></span>


<span data-ttu-id="3c51a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c51a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c51a-104">Повторный запрос источника данных, указанных в свойстве [подключение](connect-property-rds.md) и обновляет результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="3c51a-104">Requeries the data source specified in the [Connect](connect-property-rds.md) property and updates the query results.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c51a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c51a-105">Syntax</span></span>

<span data-ttu-id="3c51a-106">*DataControl*. Обновление</span><span class="sxs-lookup"><span data-stu-id="3c51a-106">*DataControl*.Refresh</span></span>

## <a name="parameters"></a><span data-ttu-id="3c51a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c51a-107">Parameters</span></span>

  - <span data-ttu-id="3c51a-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="3c51a-108">*DataControl*</span></span>

  - <span data-ttu-id="3c51a-109">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="3c51a-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c51a-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="3c51a-110">Remarks</span></span>

<span data-ttu-id="3c51a-111">Прежде чем использовать метод **Refresh** , необходимо задать свойства [подключения](connect-property-rds.md), [сервер](server-property-rds.md)и [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="3c51a-111">You must set the [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) properties before you use the **Refresh** method.</span></span> <span data-ttu-id="3c51a-112">Все элементы управления с привязкой к данным на форму, связанную с **RDS. DataControl** объекта будет содержать новый набор записей.</span><span class="sxs-lookup"><span data-stu-id="3c51a-112">All data-bound controls on the form associated with an **RDS.DataControl** object will reflect the new set of records.</span></span> <span data-ttu-id="3c51a-113">Выпущен любого существующего объекта [набора записей](recordset-object-ado.md) и не учитываются несохраненные изменения.</span><span class="sxs-lookup"><span data-stu-id="3c51a-113">Any pre-existing [Recordset](recordset-object-ado.md) object is released, and any unsaved changes are discarded.</span></span> <span data-ttu-id="3c51a-114">Метод **Refresh** автоматически преобразует первую запись текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3c51a-114">The **Refresh** method automatically makes the first record the current record.</span></span>

<span data-ttu-id="3c51a-115">Рекомендуется вызвать метод **Refresh** периодически при работе с данными.</span><span class="sxs-lookup"><span data-stu-id="3c51a-115">It's a good idea to call the **Refresh** method periodically when you work with data.</span></span> <span data-ttu-id="3c51a-116">Если извлечения данных и оставьте его на клиентском компьютере какое-то время, скорее всего, устаревший.</span><span class="sxs-lookup"><span data-stu-id="3c51a-116">If you retrieve data, and then leave it on your client machine for a while, it is likely to become out of date.</span></span> <span data-ttu-id="3c51a-117">Существует возможность, что все изменения, внесенные завершится с ошибкой, так как другому пользователю, могут измениться эту запись и отправил изменения перед выполнением.</span><span class="sxs-lookup"><span data-stu-id="3c51a-117">It's possible that any changes you make will fail, because someone else might have changed the record and submitted changes before you.</span></span>

