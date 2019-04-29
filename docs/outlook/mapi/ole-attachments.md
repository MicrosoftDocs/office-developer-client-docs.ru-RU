---
title: �������� OLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: febb6a5e-7c40-4f21-806e-7f827d1c37cf
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: fb716ce014ec3c4b21ce2b021c1a9f6f291d511c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417149"
---
# <a name="ole-attachments"></a><span data-ttu-id="b7357-103">�������� OLE</span><span class="sxs-lookup"><span data-stu-id="b7357-103">OLE Attachments</span></span>

  
  
<span data-ttu-id="b7357-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7357-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7357-p101">��������, ������� �������� ������� OLE, ���������� ��� ������� OLE 1 ����� ��� ����������� �������� �������������. ���� �������� ������ ������������� �������� �������� **IStorage** OLE 2, ������ ������ ���� ������������ � ����� OLE 1. ��� �������������� ����������� � ������� ������� **OleConvertIStorageToOLESTREAM**, ������� �������� ������ ���������� Win32 OLE.</span><span class="sxs-lookup"><span data-stu-id="b7357-p101">Attachments that are OLE objects are encoded as OLE 1 stream objects for backward compatibility. If the original object is really an OLE 2 **IStorage** object, then the object must be converted to an OLE 1 stream. This conversion is performed using the **OleConvertIStorageToOLESTREAM** function, which is part of the Win32 OLE libraries.</span></span> 
  

