---
title: HexFromBin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8f68de5e18d84c728241c188b932f99456f5be8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584837"
---
# <a name="hexfrombin"></a><span data-ttu-id="db4b9-103">HexFromBin</span><span class="sxs-lookup"><span data-stu-id="db4b9-103">HexFromBin</span></span>

  
  
<span data-ttu-id="db4b9-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db4b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db4b9-105">Преобразует двоичное число в строковое представление шестнадцатеричного числа.</span><span class="sxs-lookup"><span data-stu-id="db4b9-105">Converts a binary number into a string representation of a hexadecimal number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db4b9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="db4b9-106">Header file:</span></span>  <br/> |<span data-ttu-id="db4b9-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="db4b9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="db4b9-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="db4b9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="db4b9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="db4b9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="db4b9-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="db4b9-110">Called by:</span></span>  <br/> |<span data-ttu-id="db4b9-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="db4b9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a><span data-ttu-id="db4b9-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="db4b9-112">Parameters</span></span>

 <span data-ttu-id="db4b9-113">_pb_</span><span class="sxs-lookup"><span data-stu-id="db4b9-113">_pb_</span></span>
  
> <span data-ttu-id="db4b9-114">[in] Указатель на преобразование двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="db4b9-114">[in] Pointer to the binary data to be converted.</span></span> 
    
 <span data-ttu-id="db4b9-115">_cb_</span><span class="sxs-lookup"><span data-stu-id="db4b9-115">_cb_</span></span>
  
> <span data-ttu-id="db4b9-116">[in] Размер, в байтах, двоичных данных, на который указывает параметр _pb_ .</span><span class="sxs-lookup"><span data-stu-id="db4b9-116">[in] Size, in bytes, of the binary data pointed to by the  _pb_ parameter.</span></span> 
    
 <span data-ttu-id="db4b9-117">_sz_</span><span class="sxs-lookup"><span data-stu-id="db4b9-117">_sz_</span></span>
  
> <span data-ttu-id="db4b9-118">[out] Указатель на строку ASCII символом null, представляющее двоичные данные в шестнадцатеричных цифр.</span><span class="sxs-lookup"><span data-stu-id="db4b9-118">[out] Pointer to a null-terminated ASCII string representing the binary data in hexadecimal digits.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="db4b9-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db4b9-119">Return value</span></span>

<span data-ttu-id="db4b9-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="db4b9-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="db4b9-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="db4b9-121">Remarks</span></span>

<span data-ttu-id="db4b9-122">Функция **HexFromBin** принимает указатель на единицу двоичные данные, размер которых указывается с помощью параметра _Сертификация_ .</span><span class="sxs-lookup"><span data-stu-id="db4b9-122">The **HexFromBin** function takes a pointer to a unit of binary data whose size is indicated by the  _cb_ parameter.</span></span> <span data-ttu-id="db4b9-123">Возвращает в строке _sz_ внутри (2 \* _Сертификация_) + 1 байт памяти, представление двоичных данных в шестнадцатеричными числами.</span><span class="sxs-lookup"><span data-stu-id="db4b9-123">It returns in the  _sz_ string, within (2\*  _cb_)+1 bytes of memory, a representation of this binary information in hexadecimal numbers.</span></span> <span data-ttu-id="db4b9-124">Если значение типа byte десятичное число 10, например, шестнадцатеричную строку будет 0A, преобразуется в таком один байт два байта в строке.</span><span class="sxs-lookup"><span data-stu-id="db4b9-124">If the byte value is decimal 10, for example, the hexadecimal string will be 0A, so one byte converts to two bytes in the string.</span></span> 
  

