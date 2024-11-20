<template>
    <div class="container text-start">
        <h1 class="text-primary fw-bold">Editar</h1>
        <div class="card-header fw-bold">
        Comuna
        </div>
        <div class="card-body">
        <form @submit.prevent="updateComuna">
            <div class="row mb-3">
            <label for="comu_codi" class="form-label">Código</label>
            <div class="input-group">
                <div class="input-group-text">
                <input type="text" class="form-control" id="comu_codi" placeholder="Código comuna" disabled
                    v-model="comuna.comu_codi">
                </div>
            </div>
            </div>
            <div class="row mb-3">
            <label for="comu_nomb" class="form-label">Nombre: </label>
            <div class="input-group">
                <div class="input-group-text"><font-awesome-icon icon="building" /></div>
                <input type="text" class="form-control" id="comu_nomb" placeholder="Código comuna"
                v-model="comuna.comu_nomb">
            </div>
        </div>
        
        <div class="row mb-3">
        <label for="muni_codi" class="form-label">Municipio: </label>
        <div class="input-group">
            <div class="input-group-text"><font-awesome-icon icon="bank" /></div>
            <select class="form-select" v-model="comuna.muni_codi">
            <option v-for="municipio in municipios" v-bind:value="municipio.muni_codi">{{ municipio.muni_nomb }}</option>
            </select>
        </div>
        </div>
        <button class="btn btn-primary" type="submit">Actualizar</button>
        <button class="btn btn-secondary mx-2" @click="cancelar">Cancelar</button>
    </form>
    </div>
    </div>
</template>