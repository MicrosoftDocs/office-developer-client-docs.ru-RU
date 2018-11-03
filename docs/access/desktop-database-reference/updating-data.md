---
title: Обновление данных (Справочник по для настольных баз данных Access)
TOCTitle: Updating Data
ms:assetid: 02e82066-77c8-cbb2-db28-98e2fc94404c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248794(v=office.15)
ms:contentKeyID: 48542970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 70ca34183d135c6907a185984b02b394776bfda4
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944223"
---
# <a name="updating-data"></a><span data-ttu-id="8c9dd-102">Обновление данных</span><span class="sxs-lookup"><span data-stu-id="8c9dd-102">Updating data</span></span>


<span data-ttu-id="8c9dd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c9dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c9dd-104">Функциональность и поведение обновления во многом зависит от обновление режима (тип блокировки), тип курсора и положение курсора.</span><span class="sxs-lookup"><span data-stu-id="8c9dd-104">Update behavior and functionality is largely dependent upon update mode (lock type), cursor type, and cursor location.</span></span>

<span data-ttu-id="8c9dd-105">Используйте метод **Update** , чтобы сохранить все изменения, внесенные в текущую запись объекта **набора записей** с момента вызова метода **AddNew** или после изменения значения поля в существующей записи.</span><span class="sxs-lookup"><span data-stu-id="8c9dd-105">Use the **Update** method to save any changes you have made to the current record of a **Recordset** object since calling the **AddNew** method or since changing any field values in an existing record.</span></span> <span data-ttu-id="8c9dd-106">Объект **набора записей** должен поддерживать обновлений.</span><span class="sxs-lookup"><span data-stu-id="8c9dd-106">The **Recordset** object must support updates.</span></span>

<span data-ttu-id="8c9dd-107">Если объект **набора записей** поддерживает пакетного обновления, можно кэшировать внесение нескольких изменений в одну или несколько записей локально до вызова метода **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="8c9dd-107">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="8c9dd-108">При изменении текущей записи или добавления новой записи при вызове метода **UpdateBatch** , ADO автоматически будет вызвать метод **Update** для сохранения всех ожидающих изменений в текущей записи перед передачей пакетные изменения Поставщик.</span><span class="sxs-lookup"><span data-stu-id="8c9dd-108">If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="8c9dd-109">Текущая запись остается текущей после вызова метода **Update** или **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="8c9dd-109">The current record remains current after you call the **Update** or **UpdateBatch** methods.</span></span>

<span data-ttu-id="8c9dd-110">В этом разделе содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="8c9dd-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="8c9dd-111">Режим интерпретации</span><span class="sxs-lookup"><span data-stu-id="8c9dd-111">Immediate mode</span></span>](immediate-mode.md)
- [<span data-ttu-id="8c9dd-112">Обработка транзакций</span><span class="sxs-lookup"><span data-stu-id="8c9dd-112">Transaction processing</span></span>](transaction-processing.md)
- [<span data-ttu-id="8c9dd-113">Пакетном режиме (ADO)</span><span class="sxs-lookup"><span data-stu-id="8c9dd-113">Batch mode (ADO)</span></span>](batch-mode.md)

