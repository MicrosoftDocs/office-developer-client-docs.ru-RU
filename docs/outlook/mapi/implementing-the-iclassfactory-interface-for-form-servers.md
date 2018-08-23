---
title: Реализация интерфейса IClassFactory для серверов форм
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ff8766c6211d9820a2beed1fed871f82089b82fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566784"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a><span data-ttu-id="8d5c0-103">Реализация интерфейса IClassFactory для серверов форм</span><span class="sxs-lookup"><span data-stu-id="8d5c0-103">Implementing the IClassFactory Interface for Form Servers</span></span>

  
  
<span data-ttu-id="8d5c0-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d5c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d5c0-105">[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) является интерфейса OLE, клиентские приложения для создания новой формы объектов класса сообщений сервера форм.</span><span class="sxs-lookup"><span data-stu-id="8d5c0-105">[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) is the OLE interface that client applications use to create new form objects of your form server's message class.</span></span> <span data-ttu-id="8d5c0-106">В следующей таблице перечислены методы **IClassFactory** , которые необходимы.</span><span class="sxs-lookup"><span data-stu-id="8d5c0-106">The following table lists the **IClassFactory** methods that are required.</span></span> 
  
|<span data-ttu-id="8d5c0-107">**Способ**</span><span class="sxs-lookup"><span data-stu-id="8d5c0-107">**Method**</span></span>|<span data-ttu-id="8d5c0-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8d5c0-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d5c0-109">CreateInstance</span><span class="sxs-lookup"><span data-stu-id="8d5c0-109">CreateInstance</span></span>](http://msdn.microsoft.com/en-us/library/ms682215%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="8d5c0-110">Создает новый объект формы.</span><span class="sxs-lookup"><span data-stu-id="8d5c0-110">Creates a new form object.</span></span>  <br/> |
|[<span data-ttu-id="8d5c0-111">LockServer</span><span class="sxs-lookup"><span data-stu-id="8d5c0-111">LockServer</span></span>](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="8d5c0-112">Блокирует сервера форм в памяти, чтобы нагрузка на запуска можно избежать при создании нескольких объектов формы.</span><span class="sxs-lookup"><span data-stu-id="8d5c0-112">Locks the form server in memory so that startup overhead can be avoided when multiple form objects are created.</span></span>  <br/> |
   
<span data-ttu-id="8d5c0-113">Все сведения, необходимые для реализации этих методов см в разделе COM и службы объект ActiveX в пакете SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="8d5c0-113">For all the information necessary to implement these methods, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8d5c0-114">См. также</span><span class="sxs-lookup"><span data-stu-id="8d5c0-114">See also</span></span>



[<span data-ttu-id="8d5c0-115">Написание серверного кода формы</span><span class="sxs-lookup"><span data-stu-id="8d5c0-115">Writing Form Server Code</span></span>](writing-form-server-code.md)

