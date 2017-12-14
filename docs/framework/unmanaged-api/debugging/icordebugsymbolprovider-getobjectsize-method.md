---
title: "ICorDebugSymbolProvider::GetObjectSize 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 3c564396-ac64-4ef3-b4f6-df96f1d46fc7
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: ea9e0fcae9f98869884ad887a6c24de342512b87
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugsymbolprovidergetobjectsize-method"></a><span data-ttu-id="83c14-102">ICorDebugSymbolProvider::GetObjectSize 方法</span><span class="sxs-lookup"><span data-stu-id="83c14-102">ICorDebugSymbolProvider::GetObjectSize Method</span></span>
<span data-ttu-id="83c14-103">基于对象的 Typespec 签名返回对象的大小。</span><span class="sxs-lookup"><span data-stu-id="83c14-103">Returns the object size for an object based on its typespec signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="83c14-104">语法</span><span class="sxs-lookup"><span data-stu-id="83c14-104">Syntax</span></span>  
  
```  
HRESULT GetObjectSize(  
   [in] ULONG32 cbSignature,  
   [in, size_is(cbSignature)]  BYTE typeSig[],  
   [out] ULONG32 *pObjectSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="83c14-105">参数</span><span class="sxs-lookup"><span data-stu-id="83c14-105">Parameters</span></span>  
 `cbSignature`  
 <span data-ttu-id="83c14-106">[in] TypeSpec 签名中的字节数。</span><span class="sxs-lookup"><span data-stu-id="83c14-106">[in] The number of bytes in the typespec signature.</span></span>  
  
 <span data-ttu-id="83c14-107">typeSig</span><span class="sxs-lookup"><span data-stu-id="83c14-107">typeSig</span></span>  
 <span data-ttu-id="83c14-108">[in] TypeSpec 签名。</span><span class="sxs-lookup"><span data-stu-id="83c14-108">[in] The typespec signature.</span></span>  
  
 `pObjectSize`  
 <span data-ttu-id="83c14-109">[out] 指向对象大小的指针。</span><span class="sxs-lookup"><span data-stu-id="83c14-109">[out] A pointer to the size of the object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="83c14-110">备注</span><span class="sxs-lookup"><span data-stu-id="83c14-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="83c14-111">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="83c14-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="83c14-112">要求</span><span class="sxs-lookup"><span data-stu-id="83c14-112">Requirements</span></span>  
 <span data-ttu-id="83c14-113">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="83c14-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="83c14-114">**标头：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="83c14-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="83c14-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="83c14-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="83c14-116">**.NET framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="83c14-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="83c14-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="83c14-117">See Also</span></span>  
 [<span data-ttu-id="83c14-118">ICorDebugSymbolProvider 接口</span><span class="sxs-lookup"><span data-stu-id="83c14-118">ICorDebugSymbolProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)  
 [<span data-ttu-id="83c14-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="83c14-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)