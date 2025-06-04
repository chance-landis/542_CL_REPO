from flask import Flask, jsonify
import json

from flask_cors import CORS

app = Flask(__name__)
CORS(app)  # <-- add this line to enable CORS for all routes

def load_data():
    with open("Shop_Data.json") as f:
        return json.load(f)

data = load_data()
shops = data["shops"]

@app.route("/shops/names")
def get_store_names():
    # Return list of {id, name} objects instead of just names
    store_info = [{"id": shop["id"], "name": shop["name"]} for shop in shops]
    return jsonify(store_info)


@app.route("/shops/flavors/<int:shop_id>", methods=["GET"])
def get_flavors_by_shop(shop_id):
    for shop in shops:
        if shop["id"] == shop_id:
            flavors = shop.get("menu", {}).get("flavors", [])
            return jsonify({
                "shop": shop["name"],
                "flavors": flavors
            })
    return jsonify({"error": "Shop not found"}), 404


@app.route("/")
def info():
    return """
    Hello, I'm the Seattle Ice Cream list!
    - Visit /shops/names to get the list of all store names with IDs. Visit /shops/flavors/(insert shop ID) to recei$
    """

if __name__ == "__main__":
    app.run(debug=True)
