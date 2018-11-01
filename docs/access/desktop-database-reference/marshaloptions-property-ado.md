---
title: Свойство MarshalOptions (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f5983b7794677b5cc584c541289069acf282d9f9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883213"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="71a6e-102">Свойство MarshalOptions (ADO)</span><span class="sxs-lookup"><span data-stu-id="71a6e-102">MarshalOptions property (ADO)</span></span>


<span data-ttu-id="71a6e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="71a6e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="71a6e-104">Указывает, какие записи для маршалинга на сервере.</span><span class="sxs-lookup"><span data-stu-id="71a6e-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="71a6e-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="71a6e-105">Settings And Return Values</span></span>

<span data-ttu-id="71a6e-106">Задает или возвращает значение [MarshalOptionsEnum](marshaloptionsenum.md) .</span><span class="sxs-lookup"><span data-stu-id="71a6e-106">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value.</span></span> <span data-ttu-id="71a6e-107">Значение по умолчанию — **adMarshalAll**.</span><span class="sxs-lookup"><span data-stu-id="71a6e-107">The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="71a6e-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="71a6e-108">Remarks</span></span>

<span data-ttu-id="71a6e-109">При использовании со стороны клиента [записей](recordset-object-ado.md), записи, которые были изменены в клиенте записываются на средний уровень или веб-сервер, называемый маршалинга, процесс упаковки и отправки параметров метода интерфейса через поток или границы процессов.</span><span class="sxs-lookup"><span data-stu-id="71a6e-109">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</span></span> <span data-ttu-id="71a6e-110">Свойство **MarshalOptions** можно повысить производительность измененные удаленных данных — это упаковать для обновления в среднем уровне или в веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="71a6e-110">Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or web server.</span></span>

<span data-ttu-id="71a6e-111">**Службы удаленных данных об использовании** Это свойство используется только на стороне клиента **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="71a6e-111">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>

