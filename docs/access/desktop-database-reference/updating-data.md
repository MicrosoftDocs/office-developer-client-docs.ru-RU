---
title: Обновление данных (Справочник по для настольных баз данных Access)
TOCTitle: Updating Data
ms:assetid: 02e82066-77c8-cbb2-db28-98e2fc94404c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248794(v=office.15)
ms:contentKeyID: 48542970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8e6989468e23fc1c9c611eb091172822a6ffe938
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726339"
---
# <a name="updating-data"></a><span data-ttu-id="f6e78-102">Обновление данных</span><span class="sxs-lookup"><span data-stu-id="f6e78-102">Updating data</span></span>


<span data-ttu-id="f6e78-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6e78-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6e78-104">Функциональность и поведение обновления во многом зависит от обновление режима (тип блокировки), тип курсора и положение курсора.</span><span class="sxs-lookup"><span data-stu-id="f6e78-104">Update behavior and functionality is largely dependent upon update mode (lock type), cursor type, and cursor location.</span></span>

<span data-ttu-id="f6e78-105">Используйте метод **Update** , чтобы сохранить все изменения, внесенные в текущую запись объекта **набора записей** с момента вызова метода **AddNew** или после изменения значения поля в существующей записи.</span><span class="sxs-lookup"><span data-stu-id="f6e78-105">Use the **Update** method to save any changes you have made to the current record of a **Recordset** object since calling the **AddNew** method or since changing any field values in an existing record.</span></span> <span data-ttu-id="f6e78-106">Объект **набора записей** должен поддерживать обновлений.</span><span class="sxs-lookup"><span data-stu-id="f6e78-106">The **Recordset** object must support updates.</span></span>

<span data-ttu-id="f6e78-107">Если объект **набора записей** поддерживает пакетного обновления, можно кэшировать внесение нескольких изменений в одну или несколько записей локально до вызова метода **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="f6e78-107">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="f6e78-108">При изменении текущей записи или добавления новой записи при вызове метода **UpdateBatch** , ADO автоматически будет вызвать метод **Update** для сохранения всех ожидающих изменений в текущей записи перед передачей пакетные изменения Поставщик.</span><span class="sxs-lookup"><span data-stu-id="f6e78-108">If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="f6e78-109">Текущая запись остается текущей после вызова метода **Update** или **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="f6e78-109">The current record remains current after you call the **Update** or **UpdateBatch** methods.</span></span>

<span data-ttu-id="f6e78-110">В этом разделе содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="f6e78-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="f6e78-111">Режим немедленного обновления</span><span class="sxs-lookup"><span data-stu-id="f6e78-111">Immediate mode</span></span>](immediate-mode.md)
- [<span data-ttu-id="f6e78-112">Обработка транзакций</span><span class="sxs-lookup"><span data-stu-id="f6e78-112">Transaction processing</span></span>](transaction-processing.md)
- [<span data-ttu-id="f6e78-113">Пакетном режиме (ADO)</span><span class="sxs-lookup"><span data-stu-id="f6e78-113">Batch mode (ADO)</span></span>](batch-mode.md)

