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
ms.openlocfilehash: 12d854b72632653d9e1081c9e726c0fe7087bc27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310033"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a><span data-ttu-id="c4477-103">Реализация интерфейса IClassFactory для серверов форм</span><span class="sxs-lookup"><span data-stu-id="c4477-103">Implementing the IClassFactory Interface for Form Servers</span></span>

  
  
<span data-ttu-id="c4477-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4477-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4477-105">[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) — это интерфейс OLE, с помощью которого клиентские приложения создают новые объекты формы класса сообщений сервера форм.</span><span class="sxs-lookup"><span data-stu-id="c4477-105">[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) is the OLE interface that client applications use to create new form objects of your form server's message class.</span></span> <span data-ttu-id="c4477-106">В следующей таблице перечислены обязательные методы **IClassFactory** .</span><span class="sxs-lookup"><span data-stu-id="c4477-106">The following table lists the **IClassFactory** methods that are required.</span></span> 
  
|<span data-ttu-id="c4477-107">**Метод**</span><span class="sxs-lookup"><span data-stu-id="c4477-107">**Method**</span></span>|<span data-ttu-id="c4477-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c4477-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4477-109">CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="c4477-109">CreateInstance</span></span>](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="c4477-110">Создает новый объект Form.</span><span class="sxs-lookup"><span data-stu-id="c4477-110">Creates a new form object.</span></span>  <br/> |
|[<span data-ttu-id="c4477-111">локксервер</span><span class="sxs-lookup"><span data-stu-id="c4477-111">LockServer</span></span>](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="c4477-112">Блокирует сервер форм в памяти, чтобы избежать издержек на запуск при создании нескольких объектов формы.</span><span class="sxs-lookup"><span data-stu-id="c4477-112">Locks the form server in memory so that startup overhead can be avoided when multiple form objects are created.</span></span>  <br/> |
   
<span data-ttu-id="c4477-113">Все сведения, необходимые для реализации этих методов, представлены в разделе службы объектов COM и ActiveX в пакете Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c4477-113">For all the information necessary to implement these methods, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c4477-114">См. также</span><span class="sxs-lookup"><span data-stu-id="c4477-114">See also</span></span>



[<span data-ttu-id="c4477-115">Написание кода на сервере формы</span><span class="sxs-lookup"><span data-stu-id="c4477-115">Writing Form Server Code</span></span>](writing-form-server-code.md)

